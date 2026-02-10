# language switcher
CradleCMS language switcher web component

## Installation
Put the `alang.js` component in your themes `components` folder.

## How to use
Include the component and render the language switcher however you like inside the `<a-lang>` tag. 
It listens on a `change` event, uses the ISO-2 language code from the target value and does a page reload. 

### Example
```
{% if site.langs.size > 1 %}
{% component 'alang.js' %}
<a-lang>
    <select name="lang" class="select" value="{{lang}}">
        {%- for code in site.langs | keys | sort %}
        <option value="{{ code }}" {% if code == lang %}selected{% endif %}>{{languages[code] | t:'default' }}</option>
        {%- endfor %}
    </select>
</a-lang>
{% endif %}
```
