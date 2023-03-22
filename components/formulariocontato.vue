<template>

       <form action="" @submit.prevent="receberDados">

         <label for="nome">nome: </label>
         <input v-model="inputNome" type="text" name="" id="nome">
         <label  for="email">email: </label>
         <input v-model="inputEmail" type="text" name="email" id="email">
         <label  for="mensagem">mensagem: </label>
         <input v-model="inputMensagem" type="text" name="mensagem" id="mensagem">
         <button>enviar</button>
       
       </form>
</template>

<script>

export default{
    data:() => {
        return {
            inputNome:  "",
            inputEmail:  "",
            inputMensagem: ""

        }
  
    },
    methods: {
        receberDados() {
            const dados = {
                nome: this.inputNome,
                email: this.inputEmail,
                mensagem: this.inputMensagem,
            }
            this.$emit("enviarDados", dados)
        }
    }
}


</script>