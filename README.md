# ractive-select


A replacement for `<select>` tags that allows full styling and customizability.

### Demo

[Live Demo](http://jondum.github.com/ractive-select/demo/)

### Install


```
npm install ractive-select --save
```

### Usage

Add the select to your Ractive instance:

```js
Ractive.extend({
    ...
    components: {
        select: require('ractive-select')
    },
    ...
});
```

Use it like a normal select element

```html
<select value='{{ myValue }}'>
 {{#each options}}
 <option>{{this}}</option>
 {{/each}}
 <option>some other option</option>
</select>
```

Or if you already have an array:

```html
<select items='{{options}}'></select>
```

```js
...
data: {
    // can either be array of primitives
    items: ["foo", "bar", "baz"],

    // or array of objects with `value` and `label` -> <option value='{{value}}'>{{label}}</option>
    items: [{label: "foo", value: "_FOO", ...}],
},
...
```

### TODO

* Keyboard events — Selecting elements via string matching and up/down arrows (PRs welcome)


