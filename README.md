# language switcher
CradleCMS language switcher web component

## Installation
Put the `alang.js` component in your themes `components` folder.

## How to use
Include the component and render the language switcher however you like inside the `<a-lang>` tag. 
It listens on a `change` event, uses the ISO-2 language code from the target value and does a page reload. 

### Example
```
{% component 'alang.js' %}
{% if site.langs.size > 1 %}
<a-lang>
    <select name="lang" class="select bg-transparent w-24" value="{{lang}}">
        {% for l in site.langs | keys | sort %}
        <option value="{{ l }}" {% if l == lang %}selected{% endif %}>{{languages[l] | t:'default' }}</option>
        {% endfor %}
    </select>
</a-lang>
{% endif %}
```
