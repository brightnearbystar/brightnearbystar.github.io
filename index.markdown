---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<table>
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
  </tr>
{% endfor %}
</table>