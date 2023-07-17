<template>
    <div>
        <div v-if="working">
            <h3>Estou trabalhando no momento.</h3>
            <h2>Utilizo as seguintes tecnologias para Back-end:</h2>
            <ul>
                <li v-for="(tech, index) in backend" v-bind:key="index">{{ tech }}</li>
            </ul>
            <h2>Utilizo as seguintes tecnologias para Fron-end</h2>
            <ul>
                <li v-for="tech in frontend" :key="tech.id">
                    {{ tech.lang }}
                </li>
            </ul>
            <div>
                <button @click="showPass">{{ txtBtn }}</button>
            </div>
            <div v-show="password">
                <h4>Seu Email: {{ email }}</h4>
                <h4>Sua Senha: 1020304050</h4>
            </div>
            <p>Para acessar meu portifólio <a v-bind:href="portLink" target="_blank">Clique aqui</a> </p>
            <PicVue />
        </div>
        <div v-else>
            <h2>Em busca de trabalho </h2>
            <p v-show="showEmail">Envie um email para {{ email }} 
                com seu curriculo atualizado</p>
        </div>
    </div>
</template>

<script>
import PicVue from './form/Pic.vue'

export default {
    name: 'Info',
    components: {
        PicVue
    },
    props: {
        email: String,
        working: Boolean
    },
    data() {
        return {
            showEmail: true,
            password: false,
            portLink: 'https://google.com.br',
            txtBtn: 'Exibir Senha',
            backend: ['Javascript','Php','Python'],
            frontend: [
                //Array de Objetos
                {id: 1, lang: 'HTML'},
                {id: 2, lang: 'CSS'},
                {id: 3, lang: 'VUEJS'},
                {id: 4, lang: 'REACT'},
                {id: 5, lang: 'ANGULAR'}    
            ]
        }
    },
    methods: {
        showPass() {
           this.password = !this.password
           if(!this.password){
            this.txtBtn = 'Exibir Senha'
           }else{
            this.txtBtn = 'Ocultar Senha'
           }
        }
    }
}
</script>

<style>
/* Global style */
.p-pai{
    color:brown
}
</style>