# CSS Box-Model

There is two types `HTML` element. And all `HTML` element have some default behaviour.

```HTML
<!-- Block Level Element -->
<h1>, <p>, <div>, etc..

<!-- Inline level Element -->
<span>, <a>, <img>, etc..
```

The two types of `HTML` element are -

- Block Level Element

> **Block-Level Elements** always start from a new line and take the available width.

- Inline Level Element

> The **Inline-Level Elements** take the space as much according to the content and line up one after the other.

But how element should be display is determined by `display` property & all `HTML` element have some default `display` property.

The __Block Level Element__ have default `display` property & has value `block`.

```CSS
{
    display: block;
}
```

The __Inline Level Element__ have default `display` property & has value `inline`

```CSS
{
    display: inline
}
```

## display properties

But `display` properties contain different types of value and we can change any element behaviour from using `display` properties.

The available `display` values are `inline | block | inline-block |& more`

Example - As `h1` by default is __Block Level Element__ let change it behaviour to __Inline Level Element__

```css
h1 {
    display: inline;
}
```
