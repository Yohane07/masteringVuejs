<template>
  <h1 style="color: #00bd7e">{{nom}} {{prenom}}</h1>
  <p> qui est {{job.toUpperCase()}} avec une expertise {{expertise}}</p>
  <p> Il a plus de {{concate()}}</p>

  <a :href="lienCV"> Télécharger son cv </a>
  <p></p>
  <img :src="photo" alt="">
  <p>Quelle note lui donner: {{note}}</p>
  <div>
    <button @click="augmenterNote">+</button>
    <button @click="baisserNote">-</button>
  </div>
  <div v-bind:style="boxVbind">
    <p>On peut aussi appliquer un style,</p>
    <p>en utilisant la directive v-bind avec l'attribut style</p>
  </div>


</template>

<script>
export default{
  data() {
    return{
      nom: "ENDOKE",
      prenom: "Yohane",
      job: "Développeur FullStack",
      expertise: " en Java",
      anneeExp: 20,
      lienCV: "https://drive.google.com/drive/u/0/folders/1SkRSABfeY1I0w4Jd6BrqcIUhpJXALQLx",
      photo: "https://drive.google.com/drive/u/0/my-drive?q=type:image%20parent:0AJPIOddQaxj4Uk9PVA",
      alternative: this.prenom+this.nom,
      note: 0,
      boxVbind: {
        color: "white",
        width: "40vh",
        height: "20vh",
        backgroundColor: "red"
      }
    }
  },
  methods: {
    concate(){
      return this.anneeExp+ " ans " + this.expertise;
    },
    augmenterNote(){
      this.note++;
    },
    baisserNote(){
      this.note--;
    }
  }
}

</script>

<style scoped>

</style>