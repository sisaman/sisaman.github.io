---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD student in the School of Engineering at [École Polytechnique Fédérale de Lausanne (EPFL)](https://www.epfl.ch/en/home/) and a research assistant in the Social Computing group at [Idiap Research Institute](http://idiap.ch) under the supervision of [Prof. Daniel Gatica-Perez](https://www.idiap.ch/~gatica/). Currently, I am a visiting PhD student of the [Safe and Ethical AI programme](https://www.turing.ac.uk/research/research-programmes/artificial-intelligence-ai/safe-and-ethical) at [The Alan Turing Institute](https://www.turing.ac.uk/). Previously, I was a research intern at [Brave](https://brave.com/).

My academic research interest lies at the intersection of data privacy, trustworthy machine learning, and graph neural networks. I am a contributor to the [AI4media](https://ai4media.eu/) project, a European Union’s Horizon 2020 research and innovation program focusing on the next generation of ethical and trustworthy AI research to serve media and society.  

<!-- I am keen to initiate any kind of academic collaborations, so if you have similar research interests, please feel free to drop me a message! -->

# News

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts  limit:3  %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% include archive-single.html %}
{% endfor %}

### [See more...]({{ site.url }}/updates)
