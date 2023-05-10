{% capture pagedate %}{{ page.date | date: "%Y-%m-%d" }}{% endcapture %}
{% for row in site.data.ect.daily %}
    {% for pair in row %}
        {% if pair[0] == "Date" and pair[1] == pagedate %}
            {% assign dayrow = row %}
        {% endif %}
    {% endfor %}
{% endfor %}
