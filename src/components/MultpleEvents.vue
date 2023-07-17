<template>
  <div>
    <button @click="first(param1, $event), second(param2, $event), third()">Multiplus eventos</button>
    <p>{{ mult_events }}</p>
  </div>
</template>

<script>
export default {
    name: 'MultpleEvents',
    data(){
        return{
            mult_events: '',
            param1: 'Primeiro evento...',
            param2: 'Segundo evento...'
        }
    },
    methods: {
        first(e){
            this.mult_events = this.param1
        },
        second(e){
            setTimeout(() => this.mult_events = this.param2, 1000)
        },
        third(e){
            setTimeout(() => this.mult_events = '', 1500)
        }
    }
}
</script>

<style scoped>
    
</style>