<template>
<div>
    <form  @submit.prevent= "recebernome"> 
        <label for="nome">nome: </label>
         <input v-model="inputNome" type="text" name="dani" id="">
       <button>enviar</button>
       </form>

       <ul>
        <li v-for="nome in nomes">{{nome}}</li>
       </ul>



    </div>
</template>
<script>
export default{
   data() {
    return{
        inputNome:"",
        nomes: []
    }
   },
   methods: {
    recebernome(){
        this.nomes.push(this.inputNome)
        this.inputNome = "";
    }
   }

}
</script>






<style>
</style>