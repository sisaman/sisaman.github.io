---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am an AI Engineer in the Privacy-Preserving Machine Learning and Vision Foundation Model team at [Sony AI](https://ai.sony) Zurich, where I develop, train, and optimize state-of-the-art vision and multimodal models.
Before joining Sony, I was a research assistant in the Social Computing group at [Idiap Research Institute](http://idiap.ch) in Martigny, Switzerland.

I obtained my PhD from [EPFL](https://www.epfl.ch/en/home/), working on privacy-preserving machine learning on graphs. During my PhD, I did an internship at [Brave](https://brave.com/) and visited the [Safe and Ethical AI programme](https://www.turing.ac.uk/research/research-programmes/artificial-intelligence-ai/safe-and-ethical) at [The Alan Turing Institute](https://www.turing.ac.uk/). My research interests include trustworthy ML, computer vision, and multi-modal foundation models.

You can find more about me in my [CV](https://nbviewer.org/github/sisaman/cv/blob/master/sina-sajadmanesh-cv.pdf).


# News

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts  limit:3  %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% include archive-single.html %}
{% endfor %}

### [See more...]({{ site.url }}/updates)
