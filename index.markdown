---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<table>
  <tr>
	<th>Catalog ID</th>
	<th>Common Name</th>
	<th>RA</th>
	<th>DEC</th>
	<th>Apparent Magnitude</th>
	<th>Absolute Magnitude</th>
	<th>Stellar Class</th>
	<th>Distance</th>
	<th>Parallax [error]</th>
	<th>External Links</th>
  </tr>
{% for catalog in site.data.catalog %}
  <tr>
	<td>{{ catalog.id }}</td>
	<td>{{ catalog.name }}</td>
	<td>{{ catalog.ra }}</td>
	<td>{{ catalog.dec }}</td>
	<td>{{ catalog.app_mag }}</td>
	<td>{{ catalog.abs_mag }}</td>
	<td>{{ catalog.stellar_class }}</td>
	<td>{{ catalog.distance }}</td>
	<td>{{ catalog.parallax }}</td>
	<td>{% if catalog.links.wikipedia %}<a href="https://en.wikipedia.org/wiki/{{ catalog.links.wikipedia }}" target="_blank">Wikipedia</a>{% endif %}
	{% if catalog.links.simbad %}<br /><a href="https://simbad.u-strasbg.fr/simbad/sim-id?Ident={{ catalog.links.simbad }}" target="_blank">Simbad</a>{% endif %}
	{% if catalog.links.stellar_catalog %}<br /><span style="white-space: nowrap;"><a href="https://www.stellarcatalog.com/stars/{{ catalog.links.stellar_catalog }}" target="_blank">Stellar Catalog</a></span>{% endif %}</td>
  </tr>
{% endfor %}
</table>