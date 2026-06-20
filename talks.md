---
layout: default
title: Talks
description: Invited talks and presentations by Ting-Ting Gao.
---

# Talks & presentations

{% for talk in site.data.talks %}
<div class="entry">
  <div><span class="etype">{{ talk.type }}</span> — {{ talk.title }}</div>
  <div class="meta">{{ talk.venue }} · {{ talk.date }}</div>
</div>
{% endfor %}

## Service

<div class="entry">
  <div><span class="etype">Co-organizer</span> — <a href="https://sites.google.com/view/physnet26" target="_blank" rel="noopener">Physical Networks satellite</a></div>
  <div class="meta">NetSci 2026</div>
</div>
<div class="entry">
  <div><span class="etype">Reviewer</span> — Physical Review series, Chaos, IEEE Transactions on Network Science and Engineering, Nature Communications, and others</div>
  <div class="meta">2020 – present</div>
</div>
