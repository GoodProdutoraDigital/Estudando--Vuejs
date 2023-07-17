<template>
    <h1>Quem somos ?.. {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'byGood'
        }
    },
    //LifeCycle Hooks
    created() {
        setTimeout(() => {
            this.nome = 'Produtora'
        }, 1000)

        this.lifeCycle()
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Digital'
        }, 2000)
    },
    methods: {
        lifeCycle(){
            console.log('Executou...')
        }
    }
}
</script>