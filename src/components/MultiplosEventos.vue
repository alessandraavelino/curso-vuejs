<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro()">Ativar multiplos eventos</button>
        <p> {{multiplos_eventos}}</p>
    </div>
</template>

<script>
    export default {
        name: "MultiplosEventos",
        data() {
            return {
                multiplos_eventos: "",
                txt1: "Primeiro evento",
                txt2: "Segundo evento0"
            }
        },

        methods: {
            primeiro(txt, e) {
                e.preventDefault()
                this.multiplos_eventos = txt
                
            },
            segundo(txt, e) {
                e.preventDefault()
                setTimeout(() => this.multiplos_eventos = txt, 500)
            },

            terceiro() {
                setTimeout(() => this.multiplos_eventos = "", 1500)
            }

            
        }

    
    }
</script>