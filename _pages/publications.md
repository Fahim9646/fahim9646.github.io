---
layout: page
permalink: /publications/
title: publications
description: Published work, work under review and work in preparation.
nav: false
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

### published

<div class="publications">

{% bibliography --group_by none --query @inproceedings %}

</div>

### under review

<div class="publications">

{% bibliography --group_by none --query @misc %}

</div>

### in preparation

<div class="publications">

{% bibliography --group_by none --query @unpublished %}

</div>
