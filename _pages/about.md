---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am an AI Engineer in the Privacy-Preserving Machine Learning and Vision Foundation Model team at [Sony AI](https://ai.sony) Zurich, where I design, develop, and scale cutting-edge vision and multimodal foundation models that power real-world applications across Sony’s ecosystem. My work spans the entire lifecycle of model development—from data curation, model architecture design, and efficient training, to evaluation, performance tuning, and deployment—with a strong emphasis on scalability, efficiency, and safety.

Before joining Sony, I was a research assistant in the Social Computing group at [Idiap Research Institute](http://idiap.ch) in Martigny, Switzerland, where I worked on machine learning for social systems and privacy-aware applications.

I obtained my PhD from [EPFL](https://www.epfl.ch/en/home/), working on privacy-preserving machine learning on graphs. During my PhD, I did an internship at [Brave](https://brave.com/) and visited the [Safe and Ethical AI programme](https://www.turing.ac.uk/research/research-programmes/artificial-intelligence-ai/safe-and-ethical) at [The Alan Turing Institute](https://www.turing.ac.uk/). 

My research interests lie at the intersection of trustworthy machine learning, computer vision, and multimodal foundation models. I am particularly interested in building robust, efficient, and privacy-aware AI systems that can be reliably deployed in real-world applications.

You can find more about me in my [CV](/sina-sajadmanesh-cv.pdf).


# News

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts  limit:3  %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% include archive-single.html %}
{% endfor %}

### [See more...]({{ site.url }}/updates)
