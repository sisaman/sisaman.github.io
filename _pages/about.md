---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD student in the School of Engineering at [École Polytechnique Fédérale de Lausanne (EPFL)](https://www.epfl.ch/en/home/) and a research assistant in the Social Computing group at [Idiap Research Institute](http://idiap.ch) under the supervision of [Prof. Daniel Gatica-Perez](https://www.idiap.ch/~gatica/). I am also a member of [dhCenter](https://www.dhcenter-unil-epfl.ch/), the UNIL-EPFL joint center for digital humanities.  

My academic research interest lies at the intersection of privacy, machine learning, and social network analysis. Currently, I work on designing privacy-preserving representation learning algorithms for large-scale graphs such as social and information networks.  I contribute to the [AI4media](https://ai4media.eu/) project, a European Union’s Horizon 2020 research and innovation program focusing on the next generation of ethical and trustworthy AI research to serve media and society.  

<!-- I am keen to initiate any kind of academic collaborations, so if you have similar research interests, please feel free to drop me a message! -->

# News

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts  limit:3  %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% include archive-single.html %}
{% endfor %}

### [See more...]({{ site.url }}/updates)
