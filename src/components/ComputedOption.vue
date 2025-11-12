<template>

  <button @click ='compteurA++'>+</button>
  <button @click ='compteurA--'>-</button>
  <p v-bind:style="compteurStyle">{{compteurA}}</p>

  <hr>

  <button @click ='compteurComputed++'>+</button>
  <button @click ='compteurComputed--'>-</button>
  <p>{{compteurComputed}}</p>
  <p>{{etatCompteurMethod()}}</p>
  <p>{{etatCompteurComputed}}</p>

  <div class="box-scoped"></div>
  <div class="box-styleGlobal">Je peux l'avoir dans Composant aussi 2</div>

</template>

<script>

export default{
  data(){
    return{
      compteurA: 0,
      compteurComputed: 0,
      compteurStyle:{
        color: "red",
        fontSize: "50px"
      }
    }
  },

  methods:{
    etatCompteurMethod(){
      return this.compteurA > 5 ? 'Supérieur à 5' : 'Inférieur à 10'
    }
  },

  computed:{
    etatCompteurComputed(){
      return this.compteurA > 5 ? 'Supérieur à 5' : 'Inférieur à 10'
    }
  },

  watch: {
    compteurA(newVal){
      alert(`La nouvelle valeur du compteur est: ${newVal}`);

      setTimeout(()=> {
            alert('Comme cette valeur ne me correspond pas il n\'a existé que 5 secondes' )
            this.compteurA = 20
      }, 5000)
    }
  }
}
</script>
<!-- Scoped sur Style permet de dire que ce n'est disponible que pour ce composant,
que dans le scope où il est défini-->
<style scoped>
.box-scoped {
  background-color: burlywood;
  width: 100vh;
  height: 50vh;
}
</style>