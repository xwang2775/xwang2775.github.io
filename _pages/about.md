---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm Xinyu Jessica Wang (王昕雨)! 👋

I’m an undergraduate student at UW–Madison 🦡, passionate about Human-centered AI. I’m grateful to be working with [Bilge Mutlu](https://bmutlu.github.io/) and for the mentorship of senior student [Christine Lee](https://christineplee.github.io/) (Check out their works—you won’t regret it!).

I’m incredibly thankful to the amazing people who have inspired and guided me on this journey. 🙇‍♀️🎓

📣 I’m actively looking for Ph.D. opportunities starting Fall 2025 in Human-centered AI.

You can find my curriculum vitae [here](https://drive.google.com/file/d/1WoSETtpDUKVr9RmRANCWvNmj7TA8iufF/view?usp=drive_link).


---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="https://scholar.google.com/citations?user=tzCGmp8AAAAJ&hl=en">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}