<template>
  <div class="Counter">
    <button class="btn" @click="increment">{{ value }}</button>
  </div>
</template>

<script>
import Counter from './components/Counter'


export default {
  data () {
    return {
      value: 0
    }
  },
methods: {
  increment () {
    this.value++
  }
}
}
</script>

<style>
#app {

}
</style>
