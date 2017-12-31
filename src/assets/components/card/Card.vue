<template>
  <section class="card">
    <div class="card-titulo">
      <h3> {{ titulo }}</h3>
    </div>
    <div class="card-subtitle">
      <p> {{ subtitulo }} </p>
    </div>
    <hr>
    <div class="card-content">
      <div class="wrapper-content">
        <img :src="myImagem"> </img>
        <p> <slot> </slot> </p>
      </div>
    </div>
    <div class="card-rodape">
      <p> <slot name="rodape"> </slot> </p>
    </div>
  </section>
</template>

<script>
  export default {
    name: 'myCard',
    props: ['titulo', 'subtitulo', 'imagem'],
    data(){
       return {

      }
    },
    computed: {
      myImagem() {
        return `/src/assets/img/${this.imagem}`;
      }
    }
  }
</script>

<style scoped>
  * {
        font-family: Verdana,sans-serif;
    font-size: 1rem;
    line-height: 1.5;
  }
  .card-titulo h3{
    font-size: 1.5rem;
    margin: auto;
    line-height: 2.5;
    padding-left: 1rem;
    font-family: "Segoe UI",Arial,sans-serif;
    font-weight: 400;
  }
  .card{
    box-shadow: 0 4px 10px 0 rgba(0,0,0,0.2), 0 4px 20px 0 rgba(0,0,0,0.19);
    width: 50%;
  }
  .card-titulo{
    width:100%;
    background-color: #e0e0e0;
    min-height: 3rem;
  }
  .card-subtitle{
   }
  .card-subtitle p{
    font-family: Verdana,sans-serif;
    font-size: 1rem;
    line-height:1.5;
    padding-left: 1rem;
  }
  .card-content{

  }
  .card-content img {
    width: 11%;
    border-radius: 55px;
    float: left;
  }
  .card-content p {
    float: left;
    padding-left: 1rem;
  }
  .wrapper-content{
    min-height: 5rem;
    height:100%;
    width:95%;
    margin: auto;
  }
  .card-rodape{
    background-color:#616161;
    min-height:  2rem;
    margin-top: 1.3rem
  }

  .card-rodape p {
    text-align: center;
    color: white;
    line-height: 2;
  }
  .card-rodape:hover{
    background-color: #bfbfbf;
    cursor:pointer;
  }


  hr {
    border: 0;
    border-top: 1px solid #eee;
    margin: 20px 0;
  }
</style>
