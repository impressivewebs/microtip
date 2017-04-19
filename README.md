# Microtip.css

A modern, ultra lightweight css tooptip library. Just `1kb` minified and gzipped.

## Table of Contents
- [Installation](#installation)
- [Setup](#setup)
- [Usage](#usage)
- [Customization](#customization)

## Installation

**via npm**
	Install the package using npm:-
```
npm install microtip
```

**via yarn**
	Install the package via yarn:-
```
yarn add microtip
```

**via CDN**
	Directly include the link to the css into your project:-
```
https://unpkg.com/microtip/microtip.css
```

**direct download**
	Download the file directly from github

## Setup

**in PostCSS**
```scss
@import 'microtip';
```

**in Webpack**
```javascript
import microtip from 'microtip/microtip.min.css'
```

**in SCSS**
```scss
@import 'microtip/microtip';
```
Make sure, `node_modules` is included in the `includePaths` setting. You can then directly import the library into your file.


## Usage

Using the tooltip is incredibly simple. Simply add a custom `data-microtip` attribute to the element on which you want the tooltip to appear. The tooltip message is the attribute value. Example:-
```html
<button data-microtip="Hey tooltip!" >
```

### Position Modifiers

You can change the direction of the tooltip by adding a `data-microtip-position` attribute. The accepted values of this attribute are:- `top`, `top-left`, `top-right`, `bottom`, `bottom-left`, `bottom-right`, `left` and `right`. Example:-
```html
<button data-microtip="Hey tooltip!" data-microtip-position="top-left">
```

### Size Modifiers

By default, the tooltip will takeup only the size it requires to show the text. You can specify sizes by adding a `data-microtip-size` attribute. The accepted values include `small`, `medium`, `large` and `fit`. Example:-
```html
<button data-microtip="This is a decently long text!" data-microtip-position="top-left" data-microtip-size="medium">
```

**Note** - `fit` sets the width of the tooltip to be the same as the width on the element. It only works along with the `top` and `bottom` position modifiers.


## Customization

Microtip uses css variables, which allows you to customize the behavior of the tooltip as per your needs.

| Variable                         | Description                                        | Default Value |
|----------------------------------|----------------------------------------------------|---------------|
| `--microtip-transition-duration` | Specifies the duration of the tootltip transition  | `.18s`        |
| `--microtip-transition-delay`    | The delay on hover before showing the tooltip      | `0s`          |
| `--microtip-transition-easing`   | The easing applied while transitioning the tooltip | `ease-in-out` |

Example:-
```css
:root {
 --microtip-transition-duration: 0.5s;
 --microtip-transition-delay: 1s;
 --microtip-transition-easing: ease-out;
}
```

The above code will transition the tooltip over `0.5s` while applying an easing of type `ease-out` after a delay of `1s`

&nbsp;

<p align="center">✌️</p>
<p align="center">
<sub><sup>A little project by <a href="https://twitter.com/_ighosh">@i_ghosh</a></sup></sub>
</p>