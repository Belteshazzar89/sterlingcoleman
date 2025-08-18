{% capture pagedate %}{{ page.date | date: "%Y-%m-%d" }}{% endcapture %}
{% assign cumulative = 0 %}
{% assign dayrow = false %}
{% for row in site.data.gdr.approach-daily %}
    {% for pair in row %}
        {% if pair[0] == "Kilometers" %}
            {% assign cumulative = cumulative | plus: pair[1] %}
        {% elsif pair[0] == "Date" and pair[1] == pagedate %}
            {% assign dayrow = row %}
        {% endif %}
    {% endfor %}
    {% if dayrow != false %}
        {% break %}
    {% endif %}
{% endfor %}
