---
layout: post
title: "Some Advanced Jekyll/Liquid Template Techniques"
date: "2015-10-02"
categories: general
---

Generally speaking, Liquid templates for Jekyll are pretty easy to create - Liquid is a powerful templating tool and offers a large number of helpers and formatters to get complex tasks done. However, recently I had the opportunity to build a site that required me to use some techniques I'd never needed before with Liquid and Jekyll.

The home page had a number of repeating sections that listed the content for each category of content. If there was no content, the section shouldn't show. More importantly, each section was essentially the same except for some category metadata and styling. Rather than repeat the same code for each section, I decided to use includes - but this required some creative workarounds to make the styling show.

In this post, I'll show some of the techniques I used. I am not entirely certain that these are necessarily "best practices," but since there wasn't a lot of information I could find around the web on this, I thought it might be worth sharing. (And if you have better ways of solving these problems, please share.)

## Determining If a Category Has Posts (and How Many)

This one is actually pretty straightforward. Each category has a size property which you can use.

{% highlight liquid %}
{{ "{% if site.categories.categoryname.size"}}%}
 <!-- do something -->
{{ "{% endif"}}%}
{% endhighlight %}

Obviously, replace `categoryname` with the actual category you used for your posts. Don't worry, it won't error if the category doesn't exist. Now, I suppose you could leave the `.size` off assuming that if the category doesn't exist, that is because it contains no posts, but this works just as well (and reads easier perhaps).

## Assign the Value of a Variable

In this scenario, I had a variable that would have the current category. Assigning a variable is easy. Liquid has an `assign` keyword for this purpose.

{% highlight liquid %}
{{ "{% assign categoryname = 'foobar'"}}%}
{% endhighlight %}

Some examples claimed that you could not reassign the value of a variable once initially assigned. I didn't find this to be the case. However, you can, alternatively, assign a variable with `capture`.

{% highlight liquid %}
{%raw%}{% capture categoryname %}foobar{% endcapture %}{%endraw%}
{% endhighlight %}

## Using a Variable with an Include

There's really nothing special to do here. If the variable is assigned, you can simply use it within any include thereafter. (Note: I tried using the `with` keyword to pass the variable in the include rather than assigning it each time, but couldn't get this to work properly.)

The fun part here is that the include was always the same, just the value of the variable changed. Let's look at a small portion.

{% highlight liquid %}
{%raw%}
{% if site.categories.foobar.size %}
  {% assign categoryname = "foobar" %}
  <section>
    {% include index_article.html %}
  </section>
{% endif %}

{% if site.categories.barbar.size %}
  {% assign categoryname = "barbar" %}
  <section>
    {% include index_article.html %}
  </section>
{% endif %}
{%endraw%}
{% endhighlight %}

Within that include (which I poorly named `index_article.html`), I can loop over the posts within that category by using the variable.

{% highlight html %}
{%raw%}
{% include banner.html %}
<ul class="ArticleList">
  {% for post in site.categories[categoryname] %}
	<li>
        <h4><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h4>
        <p>{{ post.description }}</p>
        <p><span class="Author">{{ post.author }}</span>
        <span class="PublishDate">{{ post.date | date: "%b %-d, %Y" }}</span></p>
    </li>
  {% endfor %}
</ul>
{%endraw%}
{% endhighlight %}

## Dynamically Load Data

So, remember I said that the banner changed based upon some category metadata? Well, in order to do that, I decided to place the necessary metadata items in a YAML data file under `_data`. Each category had the same key name as the actual post category so that I could easily look it up. (Yes, this is probably a little brittle, but remember we are talking a static site - it's not like I'm going to push something broken live.)

Let's look at a sample of the YAML.

{% highlight yaml %}
foobar:
  name: "Foo Bar"
  description: "Foo is the best kind of bar around"
  logo: "foobar.png"
  color: "Purple"
barbar:
  name: "Bar Bar"
  description: "There's no doubt that bar is the original kind of bar"
  color: "Orange"
{% endhighlight %}

Notice that they don't all contain the exact same metadata - the first has a logo but the second doesn't. In the `index_article.html` code sample above I included `banner.html`. Let's take a look at that.

{% highlight html %}
{%raw%}
<div class="SectionHead {{ site.data.categories[categoryname].color }}Box }}">
<div class="LogoSpot">
  {% if site.data.categories[categoryname].logo %}
    <img src="{{ site.baseurl }}/images/{{ site.data.categories[categoryname].logo }}"
      alt="{{ site.data.categories[categoryname].name }}"/>
  {% elsif site.data.categories[categoryname].subtitle %}
    {{ site.data.categories[categoryname].subtitle }}
  {% else %}
    {{ site.data.categories[categoryname].name }}
  {% endif %}
</div>
<h2>{{ site.data.categories[categoryname].name }}</h2>
<h3>{{ site.data.categories[categoryname].description }}</h3>
</div>
{%endraw%}
{% endhighlight %}

Notice that I am able to dynamically pull the category name via the variable (and even though this is an include within an include after the variable was set). Also notice that I can test if particular properties exist on the category - for example I show the logo if it exists, if not the subtitle (if it exists) and else just the category name.

## Conclusion

Hopefully these examples are useful - I know they would have helped me. If anyone has suggestions on how I could have achieved the same results in a better fashion, please share.

Also, be sure to check out my free ebook from O'Reilly - [Static Site Generators - Modern Tools for Static Website Development](http://www.oreilly.com/web-platform/free/static-site-generators.csp)
