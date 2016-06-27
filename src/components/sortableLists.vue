<template lang="jade">
  .list-block.sortable
    ul
      li(v-for="(index, el) in list", :data-id="el.id", @click="onLiPress(index)")
        .item-content
          .item-media(v-if="el.img")
            img(:src="el.img")
          .item-inner
            .item-title(v-text="el.title")
            .item-after {{{el.after}}}
        .sortable-handler
</template>

<script>
  import sortable from '../js/sortable'
  import $ from '../js/Dom7'

  export default {
    props: {
      list: {
        require: true
      }
    },
    ready () {
      sortable.initSortable()
      sortable.sortableToggle('.sortable')
      $('.sortable').on('sort', () => {
        this.$dispatch('on-sort', null)
      })
    },
    methods: {
      onLiPress (index) {
        this.$dispatch('on-li-press', index)
      }
    }
  }
</script>

<style lang="less">
  @import "../less/lists.less";

</style>
