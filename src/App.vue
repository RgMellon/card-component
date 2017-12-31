<template>
  <div id="app">
  <my-card> </my-card>
  </div>
</template>

<script>
import Card from './assets/components/card/Card'
export default {
  components: {
    'myCard': Card,
  },
  name: 'app',
  data () {
    return {
    }
  }
}
</script>

<style>

</style>
