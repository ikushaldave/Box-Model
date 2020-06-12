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

Now `h1` will be behave like a `inline` element taking the space according to the content & it wrap.

Similarly we can convert a `inline` element into `block` element & this will take a all avialable width & start in new line.

Their is also special one with value of `inline-block` which is kind of hybird of both so what `inline-block` does it take space according to the content like `inline` but also we can apply padding, margin, border & it will effect to that element like `block`

Element with `display: none;` will hide the element like it is not in a `HTML` document.

## Box-Model

Every `HTML` element is rectangular box. which contain width, height, padding, border, margin & make a complete `box model`

- `width` : Every element has some default width based on the display property. If it is a block-level element it will have 100% width covering whole horizontal space. If it is an inline or inline-block element it will have width according to the content it wraps or we can specify using `width` property

- `height` : similar way every element also has some default height and that is always determined by its content.

- `padding` : The padding property provide space around the content, within an element.

- `border` : The border is to provide some outline around an element. To apply border we have border property which requires three different values: `border-width`, `border-style`, and `border-color`.

- `margin` : The border is to provide some outline around an element. To apply border we have border property which requires three different values: `border-width`, `border-style`, and `border-color`.

The Total width of any element is depend on `box-sizing` property. By default `box-sizing` have a value of `content-box`.

Total Width = Width + Padding Right + Padding left + + Border Right + Border Left + Margin Right + Margin Left

& similary `height`;

> The `content-box` follow additive of value

If we change the value of `box-sizing` property to `border-box` the width of preserve to the `border` & `margin` get add up

```CSS
/* ==========
    content-box
    total width = 300px
============ */

div {
    width: 200px;
    height: 200px;
    margin: 20px;
    border: 10px solid #f00;
    padding: 20px;
}

/* ==========
border-box
total-width = 240px
============ */

div {
    box-sizing: border-box;
}
```

## Additional Learn -

- `outline` is used to add outline outside the border & not increase size of element.

- `box-shadow` is used apply a shadow to a box

```css
div {
    box-shadow: inset(optional) horizontal vertical blur spread colour;
}
```

> How to make a solid shadow on each side you can use trick

```css

div {
    box-shadow: 0 0 0 20px #f00;
}

```

Above will do make 20px shadow outside the `border`