<template>
<div class="Test">
  <p @click="sayHello">Test {{ message }}</p>
</div>
</template>
<script>
  export default {
    data () {
      return {

      }
    },
    methods: {
      sayHello () {
    window.alert('Hello, Stephanie!')
      }
    }
  }
</script>
<style>
</style>
