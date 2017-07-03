<template>
  <div class="dialogs">
    <div class="dialog" v-bind:class="{ 'dialog-active': show }">
      <div class="dialog-content">
        <div class="close rotate">
          <span class="iconfont icon-close" @click="close"></span>
        </div>
        <slot name="header"></slot>
        <slot name="body"></slot>
        <slot name="footer"></slot>
      </div>
    </div>
    <div class="dialog-overlay"></div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        columns: [{
          name: 'ss'
        }],
        dataList: [{
          ss: 'ss1'
        }]
      }
    },
    methods: {
      loadEntry: function (key) {
        // this.$dispatch('load-entry', key)
      },
      deleteEntry: function (entry) {
        // this.$dispatch('delete-entry', entry)
      }
    }
  }
</script>
