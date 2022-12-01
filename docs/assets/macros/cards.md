{% macro start_grid(columns=3) -%}
<div class="nt-cards nt-grid cols-{{ columns }}">
{%- endmacro %}

{% macro end_grid() -%}
</div>
{%- endmacro %}

{% macro add_card(title='', content='', image='', url='') -%}
<div>
    <div class="nt-card">
        {% if url != '' %}
            <a href="{{ url }}" title="{{ title | e }}">
        {% endif  %}
        {% if image != '' %}
            <div class="nt-card-image">
                <img src="{{ image }}" class="skip-lightbox" height="105px">
            </div>
        {% endif %}
        <div class="nt-card-content">
            <p class="nt-card-title">{{ title }} </p>
        </div>
        <p class="nt-card-text">{{ content }}</p>
        {% if url != '' %}
            </a>
        {% endif %}
    </div>
</div>
{%- endmacro %}

{% macro add_image(title='', content='', image='') -%}
<div>
    <div class="nt-card">
        <div class="nt-gallery-image">
        {% if content != '' %}
            <img src="{{ image }}" data-title="{{ title | e}}" data-description="{{ content | e}}">
        {% else %}
            <img src="{{ image }}" data-title="{{ title | e }}"">
        {% endif %}
        </div>
        <div class="nt-gallery-content">
            <p class="nt-gallery-title">{{ title }} </p>
        </div>
    </div>
</div>
{%- endmacro %}
