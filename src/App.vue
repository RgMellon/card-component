<template>
  <div id="app">
  <my-card titulo="Card" subtitulo="This is sparta"
    imagem="morty.png">
    Chesssss RICK
    <span slot="rodape"> WUbbba lub dub dub </span>
  </my-card>
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
