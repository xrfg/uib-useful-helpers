# Useful helpers

## 1. Reset list mixin

Let's create a [mixin](https://sass-lang.com/documentation/at-rules/mixin) that resets a list - no padding, no margin and no list style. It should be possible to use like this:

```scss
    ul {
        @include reset-list;
    }
```

## 2. Center content

Let's create a [mixin](https://sass-lang.com/documentation/at-rules/mixin) that centers vertically and horizontally contents. It should be possible to use like this:

```scss
    @include center;
```

## 3. Hide element

Create a [mixin](https://sass-lang.com/documentation/at-rules/mixin) to hide elements - no interaction with the hidden element should be possible.
It should be possible to use like this:

```scss
    .hide {
        @include hide;
    }
```

### 4. Triangle

Let's create a mixin what creates a triangle with only CSS!
The triangle should have 3 equal sides and default size of 15px.
It should be possible to use like this, specifying the direction of the arrow:

```scss
.triangle {
    @include triangle('up')
}
```
Take a look at the [docs](https://sass-lang.com/documentation/at-rules/mixin#arguments).

**Extra:**

There should be a default color (`#000`), but I could also pass one, like this:

```scss
.triangle {
    @include triangle('up', red);
}
```

## 5. Fade in animation (extra)

Create a mixin that when included adds a fade in animation
that makes the element appear and scale. Animation should keep going forever, alternating its direction.
I should be able to use the mixing like so:

```scss
    .box {
        @include fade-in;
    }
```

Can you add custom duration to the mixin usage:

```scss
    .box {
        @include fade-in(0.5);
    }
```
> Note: we want animation, not transition.

Did you use any of the mixins you previously created?

## 6. Font sizing  (extra)

Let's define a mixin that gets a font size by its name.
We need to define a [list](https://sass-lang.com/documentation/values/maps) of available font sizes, for example:

* xs: 12px
* sm: 14px
* m: 16px
* l: 32px
* xl: 48px
* xxl: 61px

```scss
    .size-sm {
        @include font-size(xs);
    }
```

Can you also make the mixin throw an [error](https://sass-lang.com/documentation/at-rules/error) when you pass a size that does not exist in the list?

Can you also create a [function](https://sass-lang.com/documentation/at-rules/function) that gets the font size by name?

```scss
    .headline {
        font-size: font-size('l');
    }
```

## 7. Media queries (extra)

Let's create a custom media query mixin.
Take a look at the [content blocks docs](https://sass-lang.com/documentation/at-rules/mixin#content-blocks).

Breakpoints:

* m: 400px
* l: 800px
* xl: 1200

It should be possible to use like this:

```scss
.container {
    @include respond-to(tablet) {
        width: 100%;
    }
}
```