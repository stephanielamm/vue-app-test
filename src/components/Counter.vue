<template>
  <div class="Counter">
    <button class="btn" @click="increment">{{ value }}</button>
  </div>
</template>

<script>
export default {

  mounted ()  {
    console.log('Counter -> mounted.')
    this.$evt.$on('clear', this.clear)
  },

  beforeDestory () {
    console.log('Counter -> beforeDestory.')
    this.$evt.$off('clear', this.clear)
  },

  data () {
    return {
      value: 0
    }
  },
methods: {
  clear () {
    console.log('Counter -> clear.')
    this.value = 0
  },
  increment () {
    console.log('Counter -> increment.')
    this.value++
    this.$emit('increment')
  }
}
}
</script>

<style>
.Counter {

}
</style>
