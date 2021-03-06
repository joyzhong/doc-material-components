<!--docs:
title: "Cards"
layout: detail
section: components
excerpt: "<platform> Cards"
ide_version: "<cIDE name> <compatible IDE version and build number>"
material_package_version: "<compatible Material platform package version number>"
iconId:
path: /
api_doc_root:
-->

_**Instructions**_
* [Using cards](#using-cards)
    * Add a link under [Using cards](#using-cards) to your getting started page if you have one
    * Insert [installation](#installation) and [theming](#theming) as appropriate for your platform
    * Insert any additional instructions that apply to your platform with a separte level 3 header
    * If you have no getting started links or instructions, delete the [Using cards](#using-cards) sections
* [Elevated](#elevated-card) ane [Outlined](#outlined-card) sections
    * Add links to your platform 



# Cards

[Cards](https://material.io/components/cards/) contain content and actions about a single subject.

For additional information, go to the [`mdc-card` API](#mdc-card-api).

![Elevated card wtih a secondary title and two actions: Action 1 and Action 2 in purple](assets/generic-card-type-elevated.png) 


## Using cards
Before you can use a cards, you will need to install and import the following:

* Install the Material cards component
* Import JavaScript


### Install the Material card component
Install the `mdc-card` component before including it in your source.

**`mdc-card`**
```bash
npm install @material/card
```
### Import JavaScript

You can optionally add a JavaScript ripple effect (see [MDC Ripple](https://github.com/material-components/material-components-web/blob/master/packages/mdc-ripple)) to components inside yourcards by importing and then instantiating `MDCRipple` in your `*.js` file. See the page on importing the [JavaScript component](https://github.com/material-components/material-components-web/blob/master/docs/importing-js.md) for more information.

To bundle your `*.js` file, go to the [quickstart page](https://github.com/material-components/material-components-web/blob/master/docs/getting-started.md#quick-start-cdn).

<details><summary><b>Expand for instructions to add JavaScript</b></summary>

```js
import {MDCRipple} from '@material/ripple';

const selector = '.mdc-button, .mdc-icon-button, .mdc-card__primary-action';
const ripples = [].map.call(document.querySelectorAll(selector), function(el) {
  return new MDCRipple(el);
});
```

</details>


### Making cards accessible

Web's card component APIs support labeling for accessibility. To use labels...

For more guidance on writing labels, go to [our page on how to write a good accessibility label](https://material.io/design/usability/accessibility.html#writing).

### Sass mixins

Use Sass mixins when you want to customize the look and feel of your cards. Go to [sass-lang.com](https://sass-lang.com/install) for installation instructions.

<details><summary><b>Expand for instructions to use Sass mixins to customize your <code>mdc-card</code> or <code>mdc-icon-button</code></b></summary>

Before using Sass mixins for your project you will need to do the following:

* Add the Sass package to your `*.json file` under `devDependencies`:
```json
"devDependencies": {
  "sass": "^1.24.3"
}
```

* Add a `.sassrc.js` file to your project root directory:

```js
const path = require("path");

const CWD = process.cwd();

module.exports = {
  includePaths: [path.resolve(CWD, "node_modules"), path.resolve(CWD, "src")]
};
```
</details>

## Card
 
On mobile, a [card’s](https://material.io/components/cards/#specs) default elevation is 1dp, with a raised dragged elevation of 8dp.

### Card example

Source code API:
* \<platform component name\>
  * [Class definition](https://)
  * [GitHub source](https://github.com/material-components/)


The following example shows an elevated card. The card has a title, a secondary title, text, and two actions: Action 1 and Action 2 in purple (#6200EE).

<img src="assets/<platform>-elevated-card.png" alt="elevated card example for <platform> showing ...">

```
<source code here>
The source code example should display as per the interactive example (https://material.io/components/cards/#) with supporting text and Buttons:
* Display two elevated cards, for each card
* Display a card title "Card title 1" for one card and "Card title 2" for the other
* Display a secondary title "Secondary text" with an opacity of 60%
* Display text reading "Greyhound divisively hello coldly wonderfully marginally far upon excluding." with an opacity of 60%
* Display two actions, "Action 1" and "Action 2" with two text buttons
* Display the sample images ![sample card image of yellow and red tulips](assets/card-sample-image.jpg) and ![sample card image of red and yellow apples](assets/card-sample-image-2.jpg)
* Allow the cards to be moveable.
```

### Key properties

![Card anatomy diagram](assets/card-anatomy.png)

**1. Elevated card attributes**

1. **Container** 
2. **Thumbnail [optional]** 
3. **Header text [optional]** 
4. **Subhead [optional]** 
5. **Media [optional]** 
6. **Supporting text [optional]** 
7. **Buttons [optional]** <
8. **Icons [optional]** 

<b>Container</b>

Design Attribute | Theme value | Equivalent Sass mixin attribute
---|---|---
Container fill color| |
Container ink color | |
Container shape radius | |
Container outline color | |
Container outline width | | 
Container horzontal padding | | 
Container elevation | |

<b>Thumbnail (optional)</b>


|  | Attribute | Related method(s) | Default value |
|---|---|---|---|
|Desc. 1 | | | |

<b>Header text (optional)</b>

Design Attribute | Theme value | Equivalent Sass mixin attribute
---|---|---
Text label | |  
Text color | |
Typography | |

<b>Subhead (optional)</b>

Design Attribute | Theme value | Equivalent Sass mixin attribute
---|---|---
Text label | |  
Text color | |
Typography | |

<b>Media (optional)</b>


|  | Attribute | Related method(s) | Default value |
|---|---|---|---|
|Desc. 1 | | | |

<b>Supporting text (optional)</b>

Design Attribute | Theme value | Equivalent Sass mixin attribute
---|---|---
Text label | | 
Text color | |
Typography | |

<b>Button (optional)</b>


|  | Attribute | Related method(s) | Default value |
|---|---|---|---|
|Desc. 1 | | | |

<b>Icon (optional)</b>


|  | Attribute | Related method(s) | Default value |
|---|---|---|---|
|Desc. 1 | | | |


## Theming Cards

Cards support [Material Theming](https://material.io/components/cards/#theming) and can be customized in terms of color, typography and shape.

### Card theming example

API and source code

* `\<card classes\>`
  * [Class definition](https://)
  * [GitHub source](https://github.com/material-components/)

_Use the [Shrine theme](https://material.io/design/material-studies/shrine.html) for this example_
```
* Display an outlined card 
* Display a card title "Card title"
* Display a secondary title "Secondary text"
* Display text reading "Greyhound divisively hello coldly wonderfully marginally far upon excluding."
* Display two actions, "Action 1" and "Action 2" with two text buttons
* Display the sample image ![sample card image of yellow and red tulips](assets/card-sample-image.jpg)
* Make the card checkable with a "favorites" icon

```
* Make the card checkable with a "favorites" icon


## `mdc-card` API

## Style Customization

### CSS Classes

CSS Class | Description
--- | ---
`mdc-card` | Mandatory. The main card element.
`mdc-card--outlined` | Optional. Removes the shadow and displays a hairline outline instead.
`mdc-card__primary-action` | Optional. The main tappable area of the card. Typically contains most (or all) card content _except_ `mdc-card__actions`. Only applicable to cards that have a primary action that the main surface should trigger.
`mdc-card__media` | Optional. Media area that displays a custom `background-image` with `background-size: cover`.
`mdc-card__media--square` | Optional. Automatically scales the media area's height to equal its width.
`mdc-card__media--16-9` | Optional. Automatically scales the media area's height according to its width, maintaining a 16:9 aspect ratio.
`mdc-card__media-content` | Optional. An absolutely-positioned box the same size as the media area, for displaying a title or icon on top of the `background-image`.
`mdc-card__actions` | Optional. Row containing action buttons and/or icons.
`mdc-card__actions--full-bleed` | Optional. Removes the action area's padding and causes its only child (an `mdc-card__action` element) to consume 100% of the action area's width.
`mdc-card__action-buttons` | Optional. A group of action buttons, displayed on the left side of the card (in LTR), adjacent to `mdc-card__action-icons`.
`mdc-card__action-icons` | Optional. A group of supplemental action icons, displayed on the right side of the card (in LTR), adjacent to `__action-buttons`.
`mdc-card__action` | Optional. An individual action button or icon.
`mdc-card__action--button` | Optional. An action button with text.
`mdc-card__action--icon` | Optional. An action icon with no text. We recommend using [Material Icons](https://material.io/tools/icons/) from Google Fonts.

### Sass Mixins

Mixin | Description
--- | ---
`mdc-card-fill-color($color)` | Sets the fill color of a card.
`mdc-card-outline($color, $thickness)` | Sets the color and thickness of a card's outline (but does _not_ remove its shadow).
`mdc-card-shape-radius($radius, $rtl-reflexive)` | Sets the rounded shape to card with given radius size. Set `$rtl-reflexive` to true to flip radius values in RTL context, defaults to false.
`mdc-card-media-aspect-ratio($x, $y)` | Maintains the given aspect ratio on a `mdc-card__media` subelement by dynamically scaling its height relative to its width.
