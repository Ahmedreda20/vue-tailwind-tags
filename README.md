# Vue Tailwind Tags

> Only support Vue 2.0.

## Installation

### NPM

```bash
 npm install --save  vue-tailwind-tags
```

### CommonJS

```js
var VueTailwindTags = require('vue-tailwind-tags');
import 'vue-tailwind-tags/dist/vue-tailwind-tags.css';

new Vue({
  components: {
    'v-tags': VueTailwindTags,
    'tags': VueTailwindTags, // or
     ....
    // any name would you like to name to use  the component
  }
})
```

### ES6

```js
import VueTailwindTags from 'vue-tailwind-tags';
import 'vue-tailwind-tags/dist/vue-tailwind-tags.css';

new Vue({
  components: {
    VueTailwindTags,
  },
});
```

Or:

```js
import 'vue-tailwind-tags/dist/vue-tailwind-tags.css';

Vue.component('v-tags', require('vue-tailwind-tags'));
```

### Browser globals

The `dist` folder contains `vue-tailwind-tags.umd.js` and `vue-tailwind-tags.umd.min.js`

```html
<!-- css -->
<link rel="stylesheet" href="path/to/vue-tailwind-tags/dist/vue-tailwind-tags.css"></link>

<!-- javascript  -->
<script src="path/to/vue.js"></script>
<script src="path/to/vue-tailwind-tags/dist/vue-tailwind-tags.umd.js"></script>
<!-- or -->
<script src="path/to/vue-tailwind-tags"></script>

<script>
  var app = new Vue({
    el: '#app',
    components: {
      VueTailwindTags,
    },
  });
</script>
```

## Usage

```html
<VueTailwindTags v-model="tags" />
```

For more, [`see props`](#props)

> You can customize the style of the selected items [see here](#props)

## Props

| props            | default           | Type     |                                                                            |
| ---------------- | ----------------- | -------- | -------------------------------------------------------------------------- |
| value            |                   | Array    | `v-model`                                                                  |
| limit            |                   | Number   |                                                                            |
| limitText        |                   | Function | `() =>`                                                                    |
| showLimit        | `false`           | Boolean  |                                                                            |
| isOut            | `false`           | Boolean  |                                                                            |
| clearLastItem    | `true`            | Boolean  |                                                                            |
| showRemoveAll    | `true`            | Boolean  |                                                                            |
| showAddTag       | `true`            | Boolean  |                                                                            |
| styled           |                   | Object   | `{ parent: null, input: null, tag: null, button: null, remove_all: null }` |
| placeholder      | Type value here.. | String   |                                                                            |
| customValidation | `null`            | Function | `() =>` Returns a new value after checking the original value              |

## Events

| name         | params              | Type     |                        |
| ------------ | ------------------- | -------- | ---------------------- |
| @changeValue | `(value)`           | Function | `(value) =>`           |
| @input       | `(value)`           | Function | `(value) =>`           |
| @addTag      | `({ item, items })` | Function | `({ item, items }) =>` |

> want to see more features? [Contact me](https://own-portfolio-tree.vercel.app)

