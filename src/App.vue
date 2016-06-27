<template lang="jade">
  #app
    sortable-view(:list="list", @on-sort="onSort")
</template>

<script>
import sortableView from './components/sortableLists.vue'

export default {
  components: {
    sortableView
  },
  methods: {
    onSort () {
      console.log('sorted!')
    }
  },
  data () {
    return {
      list: [
        {
          title: '列表1',
          after: '列表1'
        },
        {
          title: '列表2',
          after: '列表2'
        },
        {
          title: '列表3',
          after: '列表3'
        }
      ]
    }
  },
  ready () {

  }
}
</script>

<style lang="less">
body {
  font-family: Helvetica, sans-serif;
}
</style>
