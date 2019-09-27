# Flex Responsive

## OS Compatibility

- Web browser: Chrome, Safari, Firefox, Ie 11, Edge, Opera.
- IOS: `>=9.0`.
- Android: `>=7`.

## Dependencies

- [sass-mq](https://github.com/sass-mq/sass-mq)

## Components

- `Flex`
- `Container`
- `Grid`

## Basic Usage

```html
<link
  rel="stylesheet"
  href="/node_modules/mini-flex-responsive/dist/mini-flex-responsive.min.css"
/>
```

- Or `import` sass file to your project

```scss
@import '/node_modules/mini-flex-responsive/src/index.scss';
```

- Then `overide` your variables.

### Flex

#### Variables

- `$flex-direction`: row, row-reverse, column, column-reverse;
- `$flex-wrap`: nowrap, wrap, wrap-reverse;
- `$justify-content`: flex-start, flex-end, center, space-between, space-around, space-evenly;
- `$align-items`: flex-start, flex-end, center, baseline, stretch;

#### Parts

- **Flexbox**: `flex`

  - E.g. :`flex`.

- **Flex flow**: `flex-flow-#{$flex-direction}-#{$flex-wrap}`

  - E.g. : `flex-flow-row-wrap`,`flex-flow-row-nowrap` ...

- **Flex direction**: `flex-direction-#{$flex-direction}`

  - E.g. : `flex-direction-row`, `flex-direct-row-reverse` ...

- **Flex wrap**: `flex-wrap-#{$flex-wrap}`

  - E.g. : `flex-wrap-nowrap`, `flex-wrap-wrap` ...

- **Justify content**: `justify-content-#{$justify-content}`

  - E.g. : `justify-content-center`, `justify-content-flex-end`...

- **Align Items**: `align-items-#{$align-item}`
  - E.g. : `align-items-center`, `align-items-stretch`...

### Container

#### Variables

- \$container-width: (
  `mobile`: `100%`,
  `tablet`: `720px`,
  `desktop`: `960px`,
  `wide`: `1200px`
  );
- \$gutter: `30px`;

#### Parts

- **Container**:
  - Class : `container`

### Grid

#### Variables

- \$gutter: `30px`;
- \$max-col: `12`;
- \$mq-breakpoints: (
  `mobile`: `320px`,
  `tablet`: `740px`,
  `desktop`: `980px`,
  `wide`: `1300px`
  );

#### Parts

- **Row**: `row`
- **Column**:

  - Class: `$number` from 1 to `$max-col`
    - `col`
    - `col-#{$number}`
    - `col-mobile-#{$number}`
    - `col-tablet-#{$number}`
    - `col-desktop-#{$number}`
    - `col-wide-#{$number}`

## E.g.

```html
<div
  class="flex flex-flow-row-nowrap justify-content-center align-items-center"
></div>
```

```html
<div class="container">
  <div class="row align-items-flex-end">
    <div class="col col-3 col-mobile-1 col-tablet-2"></div>
    <div class="col col-3 col-mobile-1 col-tablet-2"></div>
    <div class="col col-3 col-mobile-1 col-tablet-1"></div>
  </div>
</div>
```
