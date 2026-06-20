---
layout: default
title: About
---

<section class="hero">
  <img class="hero-photo" src="{{ '/assets/img/profile.jpg' | relative_url }}" alt="Ting-Ting Gao">
  <div class="hero-body">
    <h1>Ting-Ting Gao</h1>
    <p class="role">
      Postdoctoral Researcher,
      <strong>Center for Complex Network Research (CCNR)</strong><br>
      Northeastern University · Boston, MA
    </p>
    <ul class="tags">
      <li>Network Science</li>
      <li>Nonlinear Dynamics</li>
      <li>AI for Science</li>
      <li>Symbolic Regression</li>
      <li>Physical Networks</li>
    </ul>
    <div class="contact-links">
      <a href="mailto:{{ site.email }}">✉ Email</a>
      {% if site.scholar %}<a href="{{ site.scholar }}" target="_blank" rel="noopener">Google Scholar</a>{% endif %}
      {% if site.cv_pdf %}<a href="{{ site.cv_pdf | relative_url }}" target="_blank" rel="noopener">CV (PDF)</a>{% endif %}
      {% if site.github %}<a href="{{ site.github }}" target="_blank" rel="noopener">GitHub</a>{% endif %}
    </div>
  </div>
</section>

## About

I am a postdoctoral researcher in the
[Center for Complex Network Research (CCNR)](https://www.barabasilab.com/) at
Northeastern University, working with Prof. Albert-László Barabási. I completed
my Ph.D. in Physics at Tongji University, advised by Prof. Gang Yan.

My research sits at the intersection of **network science, nonlinear dynamics,
and machine learning**. I develop data-driven and interpretable methods to
infer, predict, and understand the dynamics of complex systems — from networked
dynamical systems and stochastic processes to physical networks and
metamaterials. A central goal of my work is to turn incomplete and noisy
observations into transparent, mechanistic models of how complex systems behave.

## News

<ul class="news">
  <li><span class="date">2026</span><span>Co-organizing the <strong>Physical Networks satellite</strong> at NetSci 2026.</span></li>
  <li><span class="date">2026</span><span>New paper on <em>Herglotz Lagrangian neural networks</em> published in <em>Physical Review Research</em>.</span></li>
  <li><span class="date">2025</span><span><em>Scale-Rich Network-Based Metamaterials</em> is under review at <em>Nature</em> (<a href="https://arxiv.org/abs/2511.18108">arXiv</a>).</span></li>
  <li><span class="date">2024</span><span>Started my postdoc in the Barabási Lab (CCNR) at Northeastern University.</span></li>
</ul>

## Selected publications

<ul class="pub-list">
{% assign selected = site.data.publications | where: "selected", true %}
{% for pub in selected %}
  <li class="pub">
    <div class="pub-title">
      {% if pub.link %}<a href="{{ pub.link }}" target="_blank" rel="noopener">{{ pub.title }}</a>{% else %}{{ pub.title }}{% endif %}
    </div>
    <div class="pub-authors">{{ pub.authors | markdownify | remove: '<p>' | remove: '</p>' }}</div>
    <div class="pub-venue"><em>{{ pub.venue }}</em>{% if pub.details %}, {{ pub.details }}{% endif %} ({{ pub.year }})</div>
  </li>
{% endfor %}
</ul>

<p><a href="{{ '/publications/' | relative_url }}">See all publications →</a></p>
