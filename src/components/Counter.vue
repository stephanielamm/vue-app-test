<template>
  <div class="Counter">
    <button class="btn" @click="increment">{{ value }}</button>
  </div>
</template>

<script>
export default {

  mounted ()  {
    console.log('Counter -> mounted.')
    // do stuff
  },

  beforeDestory () {
      console.log('Counter -> beforeDestory.')
      // do stuff
  },

  data () {
    return {
      value: 0
    }
  },
methods: {
  increment () {
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
