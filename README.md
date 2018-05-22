# vue-marquee-horizontal

> A marquee plugin for vue 

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


#Api

``` bash

<template>
    <div id="app">
        <div class="scroll"><Marquee content="这是有很多个字赶时髦地地"></Marquee></div>
    </div>   
</template>

import Css from 'vue-marquee-horizontal/dist/vue-marquee.min.css'
import Marquee from 'vue-marquee-horizontal';

export default {
    components: {
        Marquee
    },
    data() {

	}
};
```

#changelog

