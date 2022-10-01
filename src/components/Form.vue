<template>
   <div>
    <form action="" @submit="enviarForm($event)">
        <div>
            <input type="text" v-model="nome">

        </div>

        <div>
            <input type="text" v-model="email">

        </div>
        <div>
            <Submit />
        </div>
    
    </form>
   </div>

    
</template>

<script>
    import Submit from './form/Submit.vue';


export default {
    name: "Form",
    components: { Submit},

    data() {
        return {
            nome: "",
            email: ""
        }
    },

    methods: {
        enviarForm(e){
            e.preventDefault()

            const nome = this.nome;
            const email = this.email;
            console.log("dados enviados");
            console.log("o nome é " + nome);
            console.log("o email é " + email);
        }
    }

}
</script>
