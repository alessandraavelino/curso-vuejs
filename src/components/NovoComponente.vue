<template>
    <div>
        <h1>Olá mundo</h1>
        <Reutilizacao />
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>

    import MultiplosEventos from './MultiplosEventos.vue';
    import Reutilizacao from './form/Reutilizacao.vue';
    export default{
        name: "NovoComponente",
        components: { MultiplosEventos, Reutilizacao }
    }
</script>

<style scoped>
    h1 {
        color: black;
    }
</style>