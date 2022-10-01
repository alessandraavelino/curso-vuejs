<template>
    <div>
        <img :src="avatar" :alt="descricao"/>
        <MudarImagem @mudar-imagem="trocarImg"/>
    </div>
</template>

<script>
    import MudarImagem from './MudarImagem.vue';
export default {
    name: "Picture",
    components: {MudarImagem},

    data() {
        return {
            avatar: "/img/profile.png",
            descricao: "Imagem de perfil"

        }
    },

    methods: {
        trocarImg(){
            console.log("ops");
        }
    }
    
}
</script>

<style scoped>
    img {
        width: 100px;
        height: 100px;
    }
</style>