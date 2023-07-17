<template>
    <div>
        <h2>Descrição: {{ nome }}</h2>
       <Info :email="email" :working="true"/>
       <Form />
    </div>
</template>

<script>
//Reutilizando Componentes
import Info from './Info.vue'
import Form from './Form.vue'; 

export default {
    name: 'Registro',
    components: {
        Info,
        Form
    },
    data() {
        return {
            nome: 'Jefferson',
            email: 'bygood23@gmail.com'
        }
    }
}
</script>