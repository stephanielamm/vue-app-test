<template>

  <div id="app">
    <h1>{{ value }}</h1>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>

</div>
</template>

<script>
import Counter from './components/Counter'

// Need to know three component lifecycle events:
// Created, Mounted, beforeDestroy


// this.$evt.$emit (dispatch custom event)
// this.$evt.$on (add event listener)
// this.$evt.$off (remove event listener)

export default {
  name: 'app',
  components: {
    Counter
  },

data () {
  return {
    total: 0
  }
},

methods: {
  add () {
    this.total++
  },
  clear () {
    this.$evt.$emit('clear')
  }
}
}
</script>


<style>
#app {

}
</style>
