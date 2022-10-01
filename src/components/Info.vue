<template>
    <div>
        <p>Olá, sou estudante de TSI e possuo as seguintes habilidades: </p>
        <ul>
            <li>JavaScript</li>
            <li>Python</li>
            <li>Java</li>
        </ul>

        <p>{{email}}</p>
        <!--Se esta_trabalhando for igual a 'true', ele exibe o p na tela.-->
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>"Estou em busca de abrir minha empresa.</p>
        <p v-show="mostrar_email">Mnde uma mensagem para: {{ email}}</p>
        <p>Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
        <Picture />
        <p v-if="esta_logado">logado</p>
        <button @click="showEmail">Mostrar e-mail</button>
    </div>
</template>

<script>
    import Picture from './Picture.vue';

export default {
    name: "Info",
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
         
            meu_link: "https://google.com"
        };
    },

    props: ["esta_logado"],

    components: { Picture },

    methods: {
        showEmail(){
            this.mostrar_email = !this.mostrar_email
        }
    }
}
</script>
