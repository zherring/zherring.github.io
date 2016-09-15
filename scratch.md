<!--
<small>
    <a href="https://dribbble.com/zherring" target="_blank">{% include svg/ico-drb.svg %}</a>
    <a href="https://www.medium.com/my-portfolio">Medium</a>
    <a href="https://www.github.com/zherring">Github</a>
    <a href="https://www.codepen.io/zherring" target="_blank">{% include svg/ico-cp.svg %}</a>
    <a href="https://www.instagram.com/zherring" target="_blank">{% include svg/ico-ig.svg %}</a>
    <a href="https://www.twitter.com/zherring" target="_blank">{% include svg/ico-twi.svg %}</a>
    <a href="mailto:z.herring@gmail.com">{% include svg/ico-mail.svg %}</a></small>
</small>
-->


<!-- this is where we are {{ page.title }} -->
<!--
{% for pagething in site.pages %}
    {{ forloop.index }}

        {% if pagesthing.title = page.title %}
            <h1>True</h1>
        {% endif %}
    {{ pagesthing.title }}
{% endfor %}

    {% for node in site.pages %}
        {% assign next = page.index | plus: 1 %}
        {% assign prev = page.index | minus: 1 %}
        {% if prev == node.index %}
            {% assign prevPage = node %}
        {% endif %}
        {% if next == node.index %}
            {% assign nextPage = node %}
        {% endif %}
    {% endfor %}

    {% if prevPage %}
        <a href="{{ prevPage.url }}">prev: {{prevPage.title}}</a>
    {% endif %}

    {% if nextPage %}
        <a href="{{ nextPage.url }}">next: {{nextPage.title}}</a>
    {% endif %}
-->




{% for entry in site.pages %}
    {% if entry.title == page.title %}
        Match!

        index is: {{ forloop.index }} <br />

        sites.pages is {{ site.pages[forloop.index].url }} <br />
        {% assign prev = forloop.index | minus:1 %}
        {% assign next = forloop.index | plus:1 %}

        {% assign prevUrl = site.pages[prev].url %}
        {% assign nextvUrl = site.pages[next].url %}

        {% assign currentURL = site.pages[forloop.index].url %}

        previous url is: <em>{{ prevUrl }}</em> <br />
        current url is: <em>{{ currentUrl }}</em> <br />
        next url is: <em>{{ nextUrl }}</em>

        <em>prev is {{ prev }}</em>
    {% endif %}
    <br />
{% endfor %}
<!--



{% assign sorted_pages2 = site.posts %}

{% assign sorted_pages = "" | split: ""  %}
{% for item in sorted_pages2 %}
    {% if item.type == project" %}    
        {% assign sorted_pages = sorted_pages | push: item %}
    {% endif %}
{% endfor %}

{% for item in sorted_pages %}
    {% if item.url == page.url %}
        {% assign this_i = forloop.index0 %}
        {% assign num_of_pages = forloop.length %}
        {% assign last_i = forloop.length | minus: 1 %}
        {% assign next_i = forloop.index0 | plus: 1 %}
        {% assign prev_i = forloop.index0 | minus: 1 %}
    {% endif %}
{% endfor %}

{% if num_of_pages > next_i %}
    <a href="{{ sorted_pages[next_i].url }}"> Previous </a>
{% endif %}

{% if prev_i < 0 %}
    <a href="{{ sorted_pages[last_i].url }}"> Next</a>
{% endif %} -->



<!--
{% if page.layout != 'post' %}
{% assign sorted_pages2 = site.pages | sort: 'order' %}
{% else %}
{% assign sorted_pages2 = site.posts reversed %}
{% endif %}

{% assign sorted_pages = "" | split: ""  %}
{% for item in sorted_pages2 %}
    {% if item.url != "/404.html" %}    
        {% assign sorted_pages = sorted_pages | push: item %}
    {% endif %}
{% endfor %}

{% for item in sorted_pages %}
    {% if item.url == page.url %}
        {% assign this_i = forloop.index0 %}
        {% assign num_of_pages = forloop.length %}
        {% assign last_i = forloop.length | minus: 1 %}
        {% assign next_i = forloop.index0 | plus: 1 %}
        {% assign prev_i = forloop.index0 | minus: 1 %}
    {% endif %}
{% endfor %}

 -->


THIS ENDED UP working


    {% if num_of_pages > next_i %}
        <a href="{{ sorted_pages[next_i].url }}"> Next </a>
    {% else %}
        <!-- Sorted_0: {{ sorted_pages[0].url }}<br /> -->
    {% endif %}';

    {% if prev_i < 0 %}
        <!-- Sorted_Last{{ sorted_pages[last_i].url }} -->
    {% else %}
        <a href="{{ sorted_pages[prev_i].url }}">Previous</a>
    {% endif %}';
   }
