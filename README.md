# sortable-vue

Inspired by [Framework7](http://Framework7.io)

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

## 背景

今天早上日常刷知乎，之前我从来没有回答过任何问题，而今天突然看见[Vue.js如何实现拖拽排序，比如实现sortable.js这样的效果？](https://www.zhihu.com/question/46551323)这个问题，靠，这不就是我正在用的吗？立刻起床，准备把这个模块打包发出去。

实际上我从来不回答问题的原因是：我还是个小白，没有什么经验。但以后可能不会了，因为分享自己积累的过程实际上也是对自己学习的肯定，我想以后我就多学习，多做点前端的做开源吧！

哈哈，我目前也是Vue的脑残粉，上一个公司的项目被我硬生生改成用Vue来实现，我自己的项目也基本上都改成Vue了。然而还没有找到可以写Vue的下一家公司，好吧，就自己先写着玩！

## Get Started

You can directly `import` the file in the directory of `dist`, which is a packed vue component module.

````
  import sortableLists from './dist/build'

  export default {
    components: {
      sortableLists
    }
  }
````
