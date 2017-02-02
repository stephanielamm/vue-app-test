<template>

  <div id="app">
    <h1>{{ value }}</h1>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add"></Counter>
    <Counter @increment="add" v-if="false"></Counter>
    <button @click="showing =  true" >Show It</button>
      <button @click="showing =  false" >Remove It</button>

</div>
</template>

<script>
import Counter from './components/Counter'

// Need to know three component lifecycle events:
// Created, Mounted, beforeDestroy

// Created is in memory but not on the page yet.
// Mounted puts it on the page and fires it.
// In Mounted, we add listeners,
// set basic properties,
// initialize new component.
// beforeDestroy is when it leaves the page
// This is to remove listeners.


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
    this.$evt.$emit('clear'),
    this.total = 0
  }
}
}
</script>


<style>
#app {

}
</style>
