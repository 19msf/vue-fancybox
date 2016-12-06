[vue-fancybox]: https://xiecg.github.io/other/vue-fancybox/#/baseUsage

# vue-fancybox

# Overview
Image preview component based on vue.js

# DEMO

[vue-fancybox]

# Install
```Bash
npm install vue-fancybox --save
```

```JavaScript
import fancyBox from 'vue-fancybox';
```

# Base Usage

```HTML
  <div class="list" v-for="(n, index) in imageList" :data-index="index">
    <img @click="open($event)" :src="n.url" alt="">
  </div>
```

```JavaScript
export default {
  data () {
    return {
      imageList: [
        { width: 900, height: 675, url: 'http://ocm0knkb1.bkt.clouddn.com/1-1.jpg' },
        { width: 601, height: 1024, url: 'http://ocm0knkb1.bkt.clouddn.com/1-2.jpg' },
        { width: 1024, height: 700, url: 'http://ocm0knkb1.bkt.clouddn.com/1-3.jpg' }
      ]
    }
  },
  methods: {
    open (e) {
      fancyBox(e.target, this.imageList);
    }
  }
}
```