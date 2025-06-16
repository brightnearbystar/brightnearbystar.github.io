---
layout: page
title: Extras
permalink: /extras/
---

The following is a list of stars that for whatever reason did not make the current cut of the catalog. They maybe added if better information comes along.

<table>
  <tr>
	<th>Common Name</th>
	<th>Right Ascension</th>
	<th>Declination</th>
	<th>Apparent Magnitude</th>
	<th>Absolute Magnitude</th>
	<th>Stellar Class</th>
	<th>Distance</th>
	<th>Parallax [error]</th>
	<th>Reason for Exclusion</th>
	<th>External Links</th>
  </tr>
{% for extras in site.data.extras %}
  <tr>
	<td>{{ extras.name }}</td>
	<td>{{ extras.ra }}</td>
	<td>{{ extras.dec }}</td>
	<td>{{ extras.app_mag }}</td>
	<td>{{ extras.abs_mag }}</td>
	<td>{{ extras.stellar_class }}</td>
	<td>{{ extras.distance }}</td>
	<td>{{ extras.parallax }}</td>
	<td>{{ extras.reason }}</td>
	<td>{% if extras.links.wikipedia %}<a href="https://en.wikipedia.org/wiki/{{ extras.links.wikipedia }}" target="_blank">Wikipedia</a><br />{% endif %}
	{% if extras.links.simbad %}<a href="https://simbad.u-strasbg.fr/simbad/sim-id?Ident={{ extras.links.simbad }}" target="_blank">Simbad</a><br />{% endif %}
	{% if extras.links.stellar_catalog %}<span style="white-space: nowrap;"><a href="https://www.stellarcatalog.com/stars/{{ extras.links.stellar_catalog }}" target="_blank">Stellar Catalog</a></span>{% endif %}</td>
  </tr>
{% endfor %}
</table>