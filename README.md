# vue-direction

> Direction aware hover in Vue.js

## Installation

Install the component via npm by running `npm i vue-direction` or `yarn add vue-direction`.

## Usage

Import, register and place the component in your Vue app.

```html
<template>
  <VueDirection>
    <template slot-scope="{ mouseDirection }">
      <!-- do something with 'mouseDirection' -->
      {{ mouseDirection.x }}
      {{ mouseDirection.y }}
    </template>
  <VueDirection/>
</template>
```

```js
import VueDirection from 'vue-direction'

export default {
  components: {
    VueDirection,
  },
}
```

## Dev

Running `dev` script requires @vue/cli and @vue/cli-service-global to be installed. Install these globally by running `npm i --g @vue/cli @vue/cli-service-global` or `yarn add global vue/cli @vue/cli-service-global`.

## Contributing

This project is open to and encourages contributions! Feel free to discuss any bug fixes/features in the [issues](https://github.com/shwilliam/vue-direction/issues). If you wish to work on this project:

1.  [Fork the project](https://github.com/shwilliam/vue-direction/archive/master.zip)
2.  Create your feature branch (`git checkout -b new-feature-branch`)
3.  Commit your changes (`git commit -am 'add new feature'`)
4.  Push to the branch (`git push origin new-feature-branch`)
5.  [Submit a pull request!](https://github.com/shwilliam/vue-direction/pull/new/master)
