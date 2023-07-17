<template>
    <div>
        <h2>Preencha o Formulário: </h2>
        <form action="" @submit="enviarForm($event)">
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <div>
                <SubForm />
            </div>
        </form>
    </div>
</template>

<script>
import InputText from './form/InputText.vue';
import SubForm from './form/SubForm.vue';

export default {
    name: 'Form',
    components: {
        InputText,
        SubForm
    },
    data() {
        return {
            name: '',
            email: ''
        }
    },
    methods: {
        enviarForm(e){
            e.preventDefault();
            const name = this.name
            const email = this.email
            console.log(`nome: ${name} email: ${email}`)
        }
    }
}
</script>