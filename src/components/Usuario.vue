<template>
    <div>
        <h1>Olá, seja bem-vinda: {{ nome }}</h1>
        <Info :esta_logado="false" :email="email"/>
    </div>
</template>

<script>
    import Info from './Info.vue';

    export default {
        name: "Usuario",
        components: { Info},
        data () {
            return {
                nome: "Alessandra",
                email: "ale@mail.com"
                

            }
        }
    }


</script>

<style scoped>

</style>

