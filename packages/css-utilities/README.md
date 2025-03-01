# `@shopify/css-utilities`

[![Build Status](https://github.com/Shopify/quilt/workflows/Node-CI/badge.svg?branch=main)](https://github.com/Shopify/quilt/actions?query=workflow%3ANode-CI)
[![Build Status](https://github.com/Shopify/quilt/workflows/Ruby-CI/badge.svg?branch=main)](https://github.com/Shopify/quilt/actions?query=workflow%3ARuby-CI)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE.md) [![npm version](https://badge.fury.io/js/%40shopify%2Fcss-utilities.svg)](https://badge.fury.io/js/%40shopify%2Fcss-utilities.svg) [![npm bundle size (minified + gzip)](https://img.shields.io/bundlephobia/minzip/@shopify/css-utilities.svg)](https://img.shields.io/bundlephobia/minzip/@shopify/css-utilities.svg)

A set of CSS styling-related utilities.

## Installation

```bash
$ yarn add @shopify/css-utilities
```

Both `classNames` and `variationName` are helper functions that are use to generate class names.

### `classNames`

Is a straight export of [`classnames`](https://github.com/JedWatson/classnames). It returns a classNames string that are conditionally joined together.

### `variationName`

Is a utility that returns a camelCase string combining the name and value passed in.

## Usage

Given this CSS file for a `Square` React component:

```scss
.Square {
  color: transparent;
}

.sizeSmall {
  height: 20px
  width: 20px
}

.sizeLarge {
  height: 44px
  width: 44px
}

.colorWhite {
  background-color: white;
}

.colorBlack {
  background-color: black;
}
```

The following can be use to generate different class names for the component based on its props:

```tsx
type Size = 'small' | 'large';
type Color = 'white' | 'black';

interface Props {
  size: Size;
  color: Color;
}

function Square({size, color}: Props) {
  const className = classNames(
    styles.Square,
    styles[variationName<Color>('color', color)],
    styles[variationName<Size>('size', size)],
  );

  return <div className={className} />;
}
```
