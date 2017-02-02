<template>

  <div id="app">
    <h1>{{ value }}</h1>
    <Counter></Counter>
    <Counter></Counter>
    <Counter></Counter>
    <Counter></Counter>
    <Counter></Counter>

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
}
}
</script>


<style>
#app {

}
</style>
