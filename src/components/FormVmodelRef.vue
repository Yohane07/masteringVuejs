<template>
  <form @submit.prevent="onSubmit">
    <label for="txt"> Mon avis </label>
    <input type="text" id="txt">
    <button type="submit"> Envoyer</button>
  </form>
  <div class="box-styleGlobal">Je peux l'avoir dans Composant</div>
</template>

<script>
  export default{
    methods:{
      onSubmit(){
        window.alert("Votre avis a bien été partagé")
      }
    }
  }

</script>

<style scoped>

</style>