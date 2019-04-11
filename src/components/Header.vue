<template>
  <header>
    <div class="red-class" @click="clickRed">{{red}}</div>
    <div class="green-class">green</div>
    <div class="blue-class">bluea</div>
  </header>
</template>
<script>
export default {
  name: 'header-component',
  props: {},
  data () {
    return {
      color: Math.random() * 16 + 1,
      red: '红色'
    }
  },
  methods: {
    clickRed () {
      console.log(this.color)
    }
  }
}
</script>

<style lang="css" scoped="scoped">
  .red-class {
    border: 1px solid #f00;
  }

  .green-class {
    border: 1px solid #0f0;
  }

  .blue-class {
    border: 1px solid #0f0;
  }
</style>
