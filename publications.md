---
title: Publications
layout: page
---

{% assign publications = site.data.publications %}

<h1>Publications</h1>

<div class="external-databases">
<strong>External databases:</strong>
<div class="external-databases__list">
<a href="https://arxiv.org/search/?searchtype=author&query=Damiano%2C+M" target="_blank" rel="noopener noreferrer" class="external-databases__item"><img src="{{ '/assets/images/arxiv_logo.jpg' | relative_url }}" alt="arXiv logo" title="arXiv" /><span class="external-databases__label">arXiv</span></a>
<a href="https://orcid.org/0000-0002-1830-8260" target="_blank" rel="noopener noreferrer" class="external-databases__item"><img src="{{ '/assets/images/orcid_logo.png' | relative_url }}" alt="ORCID logo" title="ORCID" /><span class="external-databases__label">ORCID</span></a>
<a href="https://www.researchgate.net/profile/Mario_Damiano2" target="_blank" rel="noopener noreferrer" class="external-databases__item"><img src="{{ '/assets/images/researchgate_logo.png' | relative_url }}" alt="ResearchGate logo" title="ResearchGate" /><span class="external-databases__label">ResearchGate</span></a>
<a href="https://scholar.google.com/citations?user=UQIVvi0AAAAJ&hl=en" target="_blank" rel="noopener noreferrer" class="external-databases__item"><img src="{{ '/assets/images/google_scholar_logo.png' | relative_url }}" alt="Google Scholar logo" title="Google Scholar" /><span class="external-databases__label">Google Scholar</span></a>
<a href="https://ui.adsabs.harvard.edu/search/filter_database_fq_database=AND&filter_database_fq_database=database%3A%22astronomy%22&fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq_database=(database%3A%22astronomy%22)&p_=0&q=author%3A%22Damiano%2C%20Mario%22&sort=date%20desc%2C%20bibcode%20desc" target="_blank" rel="noopener noreferrer" class="external-databases__item"><img src="{{ '/assets/images/ads_logo.png' | relative_url }}" alt="NASA ADS logo" title="NASA ADS" /><span class="external-databases__label">NASA ADS</span></a>
<a href="{{ '/damiano.bib' | relative_url }}" download="damiano.bib" class="external-databases__item"><img src="{{ '/assets/images/bib_logo.png' | relative_url }}" alt="BibTex file icon" title="BibTex" /><span class="external-databases__label">BibTex</span></a>
</div>
</div>

{{ publications.stats.refereed_publications }} refereed publications, {{ publications.stats.first_author_papers }} first-author papers, h-index = {{ publications.stats.h_index }} (using Google Scholar)

{% for section in publications.sections %}
<h2>{{ section.title }}</h2>

<ol reversed>
  {% for entry in section.entries %}
    <li>{{ entry.authors_html }},
        <br /><i>&ldquo;{{ entry.title_html | default: entry.title }}&rdquo;</i>,
        <br /><a href="{{ entry.link_url }}">{{ entry.link_label }}</a>, {{ entry.display_date }}.
        <br /><br /></li>
  {% endfor %}
</ol>
{% endfor %}
