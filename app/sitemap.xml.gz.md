---
permalink: "sitemap.xml.gz"
eleventyExcludeFromCollections: true
---
<?xml version="1.0" encoding="utf-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  {% for page in collections.all %}
    <url>
      <loc>{{ settings.url }}{{ page.url | url }}</loc>
      <lastmod>{{ page.date | 'date_to_xmlschema' }}</lastmod>
      <changefreq>daily</changefreq>
      <priority>1.0</priority>
    </url>
  {% endfor %}
</urlset>