---
modified: 1 October 2022
---
<link rel="stylesheet" href="style.css">
<span style="font-size: 80%; color: grey;">Last modified on {{ page.modified }}</span>

Choose a version (latest first) and click on the link correspnding to your operating system.
This will download an installation file.
Open the installation file to install the software.

{% assign ver = "-" -%}
{% assign rel_by_ver = site.data.releases | sort: "key" | reverse -%}
{% for release in rel_by_ver -%}
{% if ver != release.version -%}
<span class="wt-ver">Version {{ release.version }}</span><span class="wt-date">{{ release.date }}</span>
{% endif %}
<a href="{{ release.url }}" class="wt-link">{{ release.os }}</a>{% assign ver = release.version -%}
{% endfor %}

## More information

* WaterTAP is part of the [National Alliance for Water Innovation (NAWI)](https://www.nawihub.org).
* [WaterTAP on Github](https://github.com/watertap-org/)
* [WaterTAP page on NAWI website](https://www.nawihub.org/knowledge/watertap/)

## Acknowledgements

> WaterTAP is funded by the US Department of Energy, Office of Energy Efficiency and Renewable Energy (EERE) under Funding Opportunity Announcement DE-FOA-0002336 (R&D for Advanced Water Resource Recovery)

> The National Alliance for Water Innovation (NAWI) Energy-Water Desalination Hub is funded by the U.S. Department of Energy, Energy Efficiency and Renewable Energy Office, Advanced Manufacturing Office under Funding Opportunity Announcement DE-FOA-0001905