<template>
<div class="Test">
  <p @click="sayHello">Test {{ message }}</p>
</div>
</template>
<script>
  export default {
    data () {
      return {
        message: 'my message is here.'
      }
    },
    methods: {
      sayHello () {
    this.message= 'changed message.'
      }
    }
  }
</script>
<style>
</style>
