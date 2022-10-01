<template>
    <div>
        <h1> {{nome}}</h1>
    </div>
</template>
<script>
export default {
    name: "LifeCycle",
    data() {
        return {
            nome: "testando"
        }
    },
    created () {
        setTimeout(() => {
            this.nome = "Alee"
        }, 1000)

    },

    mounted () {
        setTimeout(() => {
            this.nome = "Avelino"
        }, 2000)

    }
}
</script>

<style scoped>

</style>