---
permalink: /publications/
title: Publications
author_profile: true
publication_view: category
publication_category_order:
  - Refereed Conference Proceedings
  - Refereed Journal Publications
  - Poster Presentations
  - Preprints
---
For author list, **bold** indicates my position; *italics* indicates the names of my students and * indicates equal contribution amongst 2+ authors.

{% assign publications = site.data.publications %}
{% assign category_order = page.publication_category_order | default: "" %}
{% assign grouped_publications = publications | group_by: "category" %}
{% assign sorted_publications = publications | sort: "sort_date" | reverse %}

<style>
  .publication-view-toggle {
    display: flex;
    gap: 0.75rem;
    margin: 1.5rem 0;
    flex-wrap: wrap;
  }

  .publication-view-toggle button {
    border: 1px solid #7a8288;
    background: transparent;
    color: inherit;
    padding: 0.5rem 1rem;
    border-radius: 999px;
    cursor: pointer;
    font: inherit;
  }

  .publication-view-toggle button.is-active {
    background: #2f3e46;
    border-color: #2f3e46;
    color: #ffffff;
  }

  .publication-view-panel[hidden] {
    display: none;
  }

  .publication-entry {
    margin-bottom: 1.25rem;
  }

  .page__content .publication-entry-main,
  .page__content .publication-entry-badges,
  .page__content .publication-entry-links {
    margin: 0;
  }

  .page__content .publication-entry-badges,
  .page__content .publication-entry-links {
    margin-top: 0;
  }
</style>

<div class="publication-view-toggle" role="tablist" aria-label="Publication sorting views">
  <button type="button" class="publication-view-button" data-view="category" aria-pressed="false">Sort by category</button>
  <button type="button" class="publication-view-button" data-view="date" aria-pressed="false">Sort by date</button>
</div>

<div class="publication-view-panel" data-view-panel="category">
{% if category_order and category_order.size > 0 %}
{% for category_name in category_order %}
{% assign category_publications = publications | where: "category", category_name | sort: "sort_date" | reverse %}
{% if category_publications.size > 0 %}
<h3>{{ category_name }}</h3>
{% for publication in category_publications %}
<div class="publication-entry">
<p class="publication-entry-main">{{ publication.authors }} <a href="{{ publication.title_url }}">"{{ publication.title }}"</a>{% if publication.details %} {{ publication.details }}{% endif %}{% if publication.display_date %} {{ publication.display_date }}.{% endif %}</p>
{% if publication.badges %}
<p class="publication-entry-badges">{% for badge in publication.badges %}<span style="background-color: {{ badge.background }};color:{{ badge.color }}">{{ badge.text }}</span>{% endfor %}</p>
{% endif %}
{% if publication.links %}
<p class="publication-entry-links">{% for link in publication.links %}[<a href="{{ link.url }}">{{ link.label }}</a>]{% endfor %}</p>
{% endif %}
 </div>
{% endfor %}
{% endif %}
{% endfor %}
{% else %}
{% for category_group in grouped_publications %}
<h3>{{ category_group.name }}</h3>
{% assign category_publications = category_group.items | sort: "sort_date" | reverse %}
{% for publication in category_publications %}
<div class="publication-entry">
<p class="publication-entry-main">{{ publication.authors }} <a href="{{ publication.title_url }}">"{{ publication.title }}"</a>{% if publication.details %} {{ publication.details }}{% endif %}{% if publication.display_date %} {{ publication.display_date }}.{% endif %}</p>
{% if publication.badges %}
<p class="publication-entry-badges">{% for badge in publication.badges %}<span style="background-color: {{ badge.background }};color:{{ badge.color }}">{{ badge.text }}</span>{% endfor %}</p>
{% endif %}
{% if publication.links %}
<p class="publication-entry-links">{% for link in publication.links %}[<a href="{{ link.url }}">{{ link.label }}</a>]{% endfor %}</p>
{% endif %}
 </div>
{% endfor %}
{% endfor %}
{% endif %}
</div>

<div class="publication-view-panel" data-view-panel="date">
{% for publication in sorted_publications %}
<div class="publication-entry">
<p class="publication-entry-main">{{ publication.authors }} <a href="{{ publication.title_url }}">"{{ publication.title }}"</a>{% if publication.details %} {{ publication.details }}{% endif %}<br><small>{{ publication.category }}{% if publication.display_date %} | {{ publication.display_date }}{% elsif publication.sort_date %} | {{ publication.sort_date }}{% endif %}</small></p>
{% if publication.badges %}
<p class="publication-entry-badges">{% for badge in publication.badges %}<span style="background-color: {{ badge.background }};color:{{ badge.color }}">{{ badge.text }}</span>{% endfor %}</p>
{% endif %}
{% if publication.links %}
<p class="publication-entry-links">{% for link in publication.links %}[<a href="{{ link.url }}">{{ link.label }}</a>]{% endfor %}</p>
{% endif %}
 </div>
{% endfor %}
</div>

<script>
  (function() {
    const defaultView = {{ page.publication_view | jsonify }};
    const buttons = Array.from(document.querySelectorAll('.publication-view-button'));
    const panels = Array.from(document.querySelectorAll('.publication-view-panel'));

    function setView(view) {
      buttons.forEach((button) => {
        const active = button.dataset.view === view;
        button.classList.toggle('is-active', active);
        button.setAttribute('aria-pressed', active ? 'true' : 'false');
      });

      panels.forEach((panel) => {
        panel.hidden = panel.dataset.viewPanel !== view;
      });
    }

    buttons.forEach((button) => {
      button.addEventListener('click', function() {
        setView(button.dataset.view);
      });
    });

    setView(defaultView || 'category');
  })();
</script>