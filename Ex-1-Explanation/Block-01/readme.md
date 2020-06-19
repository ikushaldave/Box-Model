### The Box Model

Now we are more familiar with HTML & CSS. From the previous lessons, we know better about HTML elements and how they provide a simple structure to a page. We have also seen some of the common CSS properties. It's time to go a bit deeper and see how the elements are exactly displayed on a page.

In this chapter, we are going to learn about the "Box Model" of an element. We will be also looking at a few more advanced CSS properties and values.

#### Display Properties

From the earlier discussion, we know that by default there are two types of elements, block-level elements, and inline-level elements. Block-level elements always start from a new line and take the available width. The inline-level elements take the space as much according to the content and line up one after the other.

How elements are displayed, either block or inline or something else is determined by the display property. Every element has a default display property value. The common value for display property is `block, inline, inline-block, and none`. There are a few more that we will discuss later on.

However, the element's default display property can be written. A block can be displayed as inline or an inline can be displayed as a block-level element.

For example `p` is by default a block-level element, let's change its display to inline.

```
  p {
    display: inline;
  }
```

Now, the `p` element will behave as an inline-level element, taking space according to the content it wraps. Similarly, we can also convert and inline-level into a block-level element.

```
  span {
    display: block;
  }
```

By default `span` is an inline-level element, but now it is displayed as a block-level element.

There is another special kind of element, that is an inline-block level element. Things get interesting with inline-block level elements.

```
  span {
    display: inline-block;
  }
```

This value allows elements to behave as a block-level element accepting all the box-model properties(soon we gonna cover it). But at the same time, this value allows the element to lines up one after another without starting from a new line. In a simple language, you can say this value is a kind of hybrid of the block as well as inline-level elements. We will discuss more inline-block level elements, but before that, we should learn about box-model properties. After the inline-block value will make more sense.

Apart from all these values, there is one more, "none" for the display property. The "none" value will hide the element on the page as if that element does not exist in the HTML document.

```
  div {
    display: none;
  }
```

Knowing how elements are displayed on a page and how to overwrite those display value is great. It was really important, as the display of elements has implications on how the box model is rendered.

#### The Box Model

According to the box model, every element is a rectangular box on a page and it may have some width, height, padding, borders, and margins. The width, height, padding, borders, and margins are the key points of the box model, which plays an important role in deciding the size of a box on a page. It is worth important to note that every element is a rectangular box and every element has to comply with the rules of the box model.

The core of the box defined by the width and height of the box, that depends on the display property of the element, contents of the element, or specified width and height of the element in CSS. After the width and height, padding comes followed by borders, which again increase the size of the box outward. And at the last margin comes which is getting applied outside the box. Let's discuss all these box model properties one by one. After that, we will learn how to calculate the total width(actual space taken by the element horizontally) and total height(actual space taken by the element vertically).

##### Width

Every element has some default width based on the display property. If it is a block-level element it will have 100% width covering whole horizontal space. If it is an inline or inline-block element it will have width according to the content it wraps.

To set a specified width to an element we can use the width property:

```
  div {
    width: 300px;
  }
```

##### Height

As every element has some default width in a similar way every element also has some default height and that is always determined by its content. To specify the height we can use the height property:

```
  div {
    height: 300px;
  }
```

##### Padding

Padding comes after width and height, falls inside the element's border. Here is how the padding property is applied.

```
  div {
    padding: 20px;
  }
```

The padding property is applied to provide space around the content, within an element. Sometimes it is also called breathing space around the content inside the element.

In the above code `20px` of padding has been applied therefore there will be a space of 20px around the content in the box.

##### Padding Declarations

There are different ways to apply padding. We have shorthand as well as longhand properties for padding in CSS.

##### Shorthand

```
  div {
    padding: 20px;
  }
```

This is the shorthand property to apply padding on all the four sides of the element.

```
  div {
    padding: 20px 40px;
  }
```

This is another shorthand property to apply padding. The first value is for the top and bottom and the last value is for left and right padding.

To set unique values for individual side padding we can define something like this

```
  div {
    padding: 10px 0 20px 30px;
  }
```

This will be applied to all four sides with individual value. It goes clockwise. The first value is for top padding, second is for right, the third value is for the bottom and the last value is left padding of the element.

##### Longhand

In the longhand properties, we can set value for one side at a time.

```
  div {
    padding-top: 10px;
    padding-right: 0;
    padding-bottom: 20px;
    padding-left: 30px;
  }
```

##### Border

After the padding border comes. The border is to provide some outline around an element. To apply border we have border property which requires three different values: `border-width, border-style, and border-color`.

```
  div {
    border: 10px solid red;
  }
```

The above border property has shorthand values which will provide a `10px` border of red color around the element on all the four sides. In the longhand, we can apply all the above values individually.

```
  div {
    border-width: 10px;
    border-style: solid;
    border-color: red;
  }
```

To apply border on the individual side we can define individually like, `border-top, border-right, border-bottom, and border-left`.

```
  div {
    border-bottom: 10px solid #272727;
  }
```

Again here this is shorthand values for the border-bottom property. In the longhand values we can say something like this:

```
  div {
    border-bottom-width: 10px;
    border-bottom-style: solid;
    border-bottom-color: #272727;
  }
```

The width and color of the border are the normal things and can be applied normally, that we have already seen how to use the units and colors in CSS. But for the border, we have different styles.

The most common styles are `solid, double, dashed, dotted and none`. Based on these styles we can have different appearances for the border.

##### Border Radius

There is another property for the border is `border-radius`. With the help of this property, we can get a rounded or soft corner of the border. And the values can be in normal length units like pixels or percentages.

```
  div {
    border-radius: 6px;
  }
```

##### Margin

The last property in the box model is the margin. The margin property is very similar to padding. But instead of applying inside the element, it sets the space that surrounds outside the element.

```
  div {
    margin: 20px;
  }
```

Margin property is applied to provide a gap between the elements on a page. It provides space around the element. So from the above code, there will be space of 20px around the element. It can be also used to position the element on the page.

##### Margin Declarations

Margin declarations are exactly similar to padding. Whatever ways we declared padding similarly we can declare margin.

##### Shorthand

```
  div {
    margin: 20px;
  }
  div {
    margin: 10px 20px;
  }
  div {
    margin: 0 10px 15px 20px;
  }
```

##### Longhand

```
  div {
    margin-top: 0;
    margin-right: 10px;
    margin-bottom: 15px;
    margin-left: 20px;
  }
```

These are different "Box Model" properties that decide an element's size on a page. Let's apply all these box model properties together on an element. Let's take one block-level and one inline-level element and then experiment with all these properties.

#### Box Model Properties on Block-Level Element

```
  div {
    width: 300px;
    height: 260px;
    padding: 20px;
    border: 10px solid blue;
    margin: 20px;
  }
```

By default `div` is a block-level element and all the box model property will work normally on block-level elements. Whatever the value you will apply for these properties on the block-level element, you will see the result as expected.

However, there is just one oddity with margin on block-level elements. The vertical margin on block-level elements gets collapsed. Let's understand this with an example. Suppose we have two paragraph elements. By default, p is a block-level element.

```
  <p>.........</p>
  <p>.........</p>

  p {
    margin: 20px;
  }
```

Normally both the paragraph elements will be having a margin of 20px all around it. But the vertical margin between the elements will be also 20px only. Ideally, it should be 40px, 20px bottom margin of the first paragraph element and 20px top margin of the second paragraph element. This is known as collapsing of a vertical margin between the block elements. Sometimes we can see something like this also

```
  <p class="para1">.........</p>
  <p class="para2">.........</p>
  .para1 {
    margin-bottom: 30px;
  }
  .para2 {
    margin-top: 70px;
  }
```

Ideally, the vertical margin between the para1 and para2 should be 100px, but it will be 70px. Because smaller margin always gets collapsed into the bigger one.

#### Box Model Properties on Inline-Level Element

```
  span {
    width: 300px;
    height: 260px;
    padding: 20px;
    border: 10px solid blue;
    margin: 20px;
  }
```

By default `span` is an inline-level element. When you will apply all these box model properties on an inline-level element, you won't find the result as expected. The box model properties do not work normally on inline-level elements.

##### Width and Height

The inline-level element does not accept `width` and `height` property. Always keep this in mind while working with the inline-level element. The inline-level element always takes the width and height according to the content.

##### Padding

Padding for inline-level elements works a bit differently. It works on all four sides but with some exceptions. The vertical padding( top and bottom) may blend into the line of above and below elements but will be displayed. The left and right padding will work normally.

##### Border

Similar to padding, you may also find the `border-top` and `border-bottom` gets blend into the line of above and below elements but will be displayed.

##### Margin

When it comes to applying margin on inline elements, we have something different behavior than the block elements. In inline elements, the horizontal margin(left and right) works normally. But the vertical margins are ignored on inline elements. The inline-level elements do not accept vertical(top and bottom) margin.

We have familiarized ourselves with all the box model properties. We have seen all these properties works based on block-level as well as inline-level elements. Look at the table below you will get even more clear idea, how inline-level element differ from block-level elements.

![Table for block and inline-level element on box model properties](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/box-model/box-model-table.png)

Now that we know that the inline-level elements do not accept all the box model properties. Therefore there is another value for `display` property, `inline-block`. I have already introduced the `inline-block` elements above. Now, its time to go a bit deeper.

#### Inline Block Elements

The inline-block value allows an element to behave as a block-level element accepting all the box model properties. But at the same time, the element will take the space according to the content it wraps, similar to inline-level elements. This value comes handy, whenever you need your elements lines up one after another, also you want to apply all the box model properties.

```
  span {
    display: inline-block;
    width: 300px;
    height: 260px;
    padding: 20px;
    border: 10px solid blue;
    margin: 20px;
  }
```

By default, span is an inline-level element and it will not accept all the box model properties. But as we have overwritten it's display property to inline-block, therefore now the span will accept all the box model properties without any exception.

##### Removing Space between the inline-block elements.

It is good to make an element as an inline-block whenever you need your elements to line up one after another, accepting all the box-model properties. But sometime you may encounter a problem that is inline-block elements are not always touching when they line up one after another. You'll always find a small space between the inline-block elements. That space may disturb the flow of the content.

There are different ways to get rid of those small spaces. Let's try a few of them: One we can set the parent's(containing inline-block elements) font-size to 0. But here again, we will have to set the font-size for children according to the need.

```
  <div class="parent">
    <div class="inline-block>.....</div>
    <div class="inline-block>.....</div>
    <div class="inline-block>.....</div>
  </div>

  .parent {
    font-size: 0;
  }
  .inline-block {
    display: inline-block;
    font-size: 16px;
  }
```

The other two ways can be applied in HTML to remove space. One we can place the opening tag of each new inline-block element just after the closing tag of the previous inline-block element.

```
  <div class="inline-block>
    .......
  </div><div class="inline-block>
    .......
  </div><div class="inline-block>
    .......
  </div>
```

And the last way is to open HTML comment just after the closing tag of an inline-block element and then close the HTML comment just before the opening tag of the next inline-block element.

```
  <div class="inline-block>
    .......
  </div><!--
  --><div class="inline-block>
    .......
  </div><!--
  --><div class="inline-block>
    .......
  </div>
```

All options work fine. It is entirely upon which you choose.

#### Calculating the width and height of an element.

Remember, in the beginning, we talked that according to the box model every element is a rectangular box and all the box model properties determine the size of that box.

Now as we have a better knowledge of all the box model properties, let's calculate the total width and height of an element.

```
  div {
    width: 400px;
    height: 280px;
    padding: 20px;
    border: 10px solid blue;
    margin: 20px;
  }
```

According to the box model the total width of an element can be calculated using formula:

`marging-left + border-left + padding-left + width + padding-right + border-right + margin-right`

And total height can calculated using formulat:

`marging-top + border-top + padding-top + width + padding-bottom + border-bottom + margin-bottom`

Using the above formula we can find out the total width and height of the div used in the above code.

`Total Width: 20px + 10px + 20px + 400px + 20px + 10px + 20px = 500px`

`Total Height: 20px + 10px + 20px + 280px + 20px + 10px + 20px = 380px`

The box model topic is one of the most confusing topics in HTML & CSS. Just now you saw we applied width and height 400px and 280px respectively, but in the end, we got total width 500px and total height 380px.

By default all the box model properties are additive. That means to determine the actual width and height of an element we will have to take into account padding, borders, and margins of all the four sides. The total width of an element not only decided by the width property but also the left and right padding, left and right borders, and left and right margins. The same goes for height, top and bottom padding, top and bottom borders, and top and bottom margins.

> #### Outline
>
> Apart from all the box model properties, there is a property, `outline`, that draws a line around the elements, outside the borders.
>
> ```
>   div {
>     outline: 10px solid blue;
>   }
> ```
>
> The `outline` property is very similar to `border` property except:
>
> 1. It’s not a part of the box model, so it won’t affect the position of the element or adjacent elements.
>    Also it is not counted while calculating the size of an element.
>
> 2. You can’t set an outline on just one (or two, or three) sides of an element.
>    All sides only.
>    There is no such thing as outline-top, outline-right, outline-bottom, or outline-left like there is with border.

#### The Box Sizing Property

As far as we know that all the box model properties are additive. To determine the actual size of an element we need to take into account all the box model properties. That's the default box model of an element.

However, we can change the default box model of an element. In CSS there is another property, `box-sizing` which allows us to change how the box model works and how an element's size is calculated. The `box-sizing` property accepts two different values, `content-box` and `border-box`.

##### Content Box

The `content-box` value for the `box-sizing` property is the default value, that leaves box model property additive only. If we do not specify any `box-sizing` property for an element, that means the model is still `content-box`.

```
  div {
    box-sizing: content-box;
  }
```

In content box after the width and height, whatever the extra properties padding, borders, or margins we define will get added to determine the exact size of the box.

##### Border Box

Border box value changes the box model. It keeps the padding and border within the specified width and height. If an element has a width of 300px, padding of 20px, and border around it is 10px, the actual width will remain 300px only.

```
  div {
    width: 300px;
    padding: 20px;
    border: 10px solid #272727;
    box-sizing: border-box;
  }
```

So, here according to the border-box value the div will be having a width of 300px instead of 360px.

But if we add any margin it will be added to the specified width of the element. So, in both cases, whether it is a content-box or a border-box, the margins are always added to calculate the actual size of the box.

> #### Box Shadow
>
> There is one more property, box-shadow, used to create a shadow effect around the element.
>
> ```
>   div {
>     box-shadow: 3px 3px 6px 1px rgba(0, 0, 0, 0.3);
>   }
> ```
>
> The property generally accepts five values.
> The first four values are for creating length and height of shadow and the last value is for the color of the shadow.
> The first value is for the shadow's offset in the horizontal direction, the second value is for the shadow's offset in the vertical direction, the third value is for blur radius.
> The third value determines how blurry the shadow will look.
> The fourth value is to spread the shadow in all directions. This is the optional value, without this also we can create a shadow.
>
> ```
>   div {
>     box-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
>   }
> ```
>
> Multiple shadows can also be created on one element.
> To create multiple shadows just need to add comma separated values.
>
> ```
>   div {
>     box-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3), 6px 6px 10px rgba(0, 0, 0, 0.3);
>   }
> ```
>
> If we provide the values in negative then it will create a shadow in the opposite direction.
>
> ```
>   div {
>     box-shadow: -3px -3px 6px rgba(0, 0, 0, 0.3);
>   }
> ```
>
> To create some solid line around the box using box-shadow we can only provide spread value and color value. Rest of the value will be 0.
>
> ```
>   div {
>     box-shadow: 0 0 0 3px #000;
>   }
> ```
>
> All the above box-shadow values will create the shadow outside the box, but if you want to create the shadow inside the box you can just add inset at the starting of the value.
>
> ```
>   div {
>     box-shadow: inset 3px 3px 6px rgba(0, 0, 0, 0.3);
>   }
> ```

#### Developer Tools

Most of the browsers come with Developer Tools to inspect elements on a page. It helps us to see all the CSS properties that have been applied on an element also it let us know where the element is sitting in the HTML document.

To open a Developer Tools right click on the page, you will get an option to inspect. Once you click the inspect option, this will open a new window that provides a handful of tools to inspect elements.

![Developer Tools](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/box-model/developer-tools.png)

The inspect window has HTML elements on the left side and the right side style related to the HTML elements. In Chrome, on the top left corner of the inspect window, you also get a button to select any element on the page. Clicking that button you can select any element on the page by clicking on it. Once you select an element on the page, all the styles related to that element will be revealed on the right side.

On the right-hand side, you will also see a few tabs within Developer Tools. If you select 'computed' a break down of the box model will open of the selected element. That's the real box model of an element on a page. Here you will find all box model properties(width, height, padding, borders, and margins) defined for the element. This box model defines the exact size of the box on a page.

![Box Model of an Element](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/box-model/computed.png)

The Developer tools are one most frequently used tools by the developer. There are a lot more things can be done in developer tools.

The "Box Model" is one of the most confusing topics in HTML & CSS. But I would suggest do not move further until and unless you master this topic. Because this topic is a powerful part of HTML & CSS. If you have a better knowledge of the box model, the rest of the topic will be easy for you to pick up.
