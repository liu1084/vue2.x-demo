<template>
  <div @click="clickMe" ref="footer" :class="backgroundColor">
    {{ footerText }}
    <div @click.stop.prevent="changeVersion">
      {{version}}
    </div>
  </div>
</template>
<script>
export default {
  name: 'v-footer',
  data () {
    return {
      footerText: 'this is a footer;',
      backgroundColor: ''
    }
  },
  props: {
    version: Number,
    license: String
  },
  methods: {
    clickMe () {
      // this.$ref.footer.class = 'red'
      this.backgroundColor = 'red'
    },
    changeVersion () {
      this.$emit('onChange', 3)
    }
  }
}
</script>
<style>
  .red {
    background: #f00;
  }
</style>
