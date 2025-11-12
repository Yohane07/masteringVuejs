<template>
  <div>
      <button @click.once="console">Je le recommande au vu de son parcours</button>
  </div>
  <div class="box-styleGlobal">Je peux l'avoir dans Composant Aussi 3</div>
</template>

<script>
  export default{
    methods: {
      console(){
        console.log("Je le recommande")
    }
    }

  }

</script>

<style scoped>

</style>