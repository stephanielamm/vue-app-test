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
    this.++
  }
}
}
</script>


<style>
#app {

}
</style>
