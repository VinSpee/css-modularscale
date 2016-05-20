# Modular Scale

A modular scale is a list of values that share the same relationship. These values are often used to size type and create a sense of harmony in a design. Proportions within modular scales are all around us from the spacing of the joints on our fingers to branches on trees. These natural proportions have been used since the time of the ancient Greeks in architecture and design and can be a tremendously helpful tool to leverage for web designers.

Ems work especially well with modular scales as their recursive properties mimic modular scales making them more predictable and easier to manage. Pixels and other units work just fine and breakpoints in responsive web design can naturally fall on your scale to create better relevance to your text as all the values in your layout harmonize with each other.

To get started, you need to select a ratio and a base value. The base value is usually your text font size or 1em. This base size paired with a ratio such as the golden ratio or any musical proportion will create your scale of values which all share this proportion.

## Install
- `npm install css-modularscale`
- then, in your css:
	`@import "css-modularscale"`

## Compatability
`css-modularscale` is created with future CSS syntax in mind. For more information about CSS variables and the spec, consult [The W3C's Working Draft on the topic](http://www.w3.org/TR/css-variables/).
You can use any CSS "postprocessor" that has support for custom properties, such as [PostCSS](https://github.com/postcss) or [Rework](https://github.com/reworkcss/). If you want to get started fast, I recommend checking out the [CSSNext project](https://github.com/cssnext/cssnext).

## Usage

Modular Scale has two default variables that you should place with your other site wide variables. `--ms-base` is usually your font size or `1rem`. `--ms-ratio` is the factor of change between each number so if the ratio is `1.5` then each number in the sequence will be 1.5 times that of the previous number.

```css
:root {
	--ms-base: 1em;
	--ms-ratio: var(--golden);
}
```

Modular-scale is used as a custom property. Simply pass it through in place of any value to use a value based on a modular scale.

```scss
font-size: var(--ms2); // two up the modular scale
```

## Ratios

Modular scale includes functions for a number of classic design and musical scale ratios. You can add your own ratios as well.

By default, the variable `--ms-ratio` is set to `--golden`.

<table>

  <tr><th>Function</th><th>Ratio</th><th>Decimal value</th></tr>

  <tr><td>--phi</td><td>1:1.618</td><td>1.618</td></tr>
  <tr><td>--golden</td><td>1:1.618</td><td>1.618</td></tr>
  <tr><td>--double-octave</td><td>1:4</td><td>4</td></tr>
  <tr><td>--major-twelfth</td><td>1:3</td><td>3</td></tr>
  <tr><td>--major-eleventh</td><td>3:8</td><td>2.667</td></tr>
  <tr><td>--major-tenth</td><td>2:5</td><td>2.5</td></tr>
  <tr><td>--octave</td><td>1:2</td><td>2</td></tr>
  <tr><td>--major-seventh</td><td>8:15</td><td>1.875</td></tr>
  <tr><td>--minor-seventh</td><td>9:16</td><td>1.778</td></tr>
  <tr><td>--major-sixth</td><td>3:5</td><td>1.667</td></tr>
  <tr><td>--minor-sixth</td><td>5:8</td><td>1.6</td></tr>
  <tr><td>--fifth</td><td>2:3</td><td>1.5</td></tr>
  <tr><td>--augmented-fourth</td><td>1:√2</td><td>1.414</td></tr>
  <tr><td>--fourth</td><td>3:4</td><td>1.333</td></tr>
  <tr><td>--major-third</td><td>4:5</td><td>1.25</td></tr>
  <tr><td>--minor-third</td><td>5:6</td><td>1.2</td></tr>
  <tr><td>--major-second</td><td>8:9</td><td>1.125</td></tr>
  <tr><td>--minor-second</td><td>15:16</td><td>1.067</td></tr>

</table>

Add your own ratio in CSS by setting a variable and passing that to modular-scale.

```css
:root {
	--my-ratio: calc(1 / 3.14159265);
	--ms-ratio: var(--my-ratio);
}
```

## [Changelog](https://github.com/VinSpee/css-modular-scale/releases)
