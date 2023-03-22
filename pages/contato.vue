 <template> 


    <h1> pagina de contato </h1>
    <Formulariocontato
    @enviarDados="receberdados"
    /> 
    <hr>
    <p> lista de contatos:</p>
    
        <ul v-for="ct in Object.keys(listacontato)"> 
        <li> nome: <strong> {{ listacontato [ct].nome}} </strong></li> 
        <li> email <strong> {{ listacontato [ct].email}} </strong></li>
        <li> mensagem: <strong>{{ listacontato [ct].mensagem}}</strong></li>
        <hr>
 
    </ul>
 </template>

<script>

export default {
      data (){
        return {
        listacontato: [
            {
                "nome": "dani",
                "email": "danihprado06@gmail.com",
                "mensagem": "mensagem..."
            },

            {
                "nome": "victor",
                "email": "victor@gmail.com",
                "mensagem": "mensagem2"
            },
        ]

      }

    },
    methods:{
        receberdados(dados){
            console.log(dados)
            this.listacontato.push(dados)
        }
    }

}

</script>