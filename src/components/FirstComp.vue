<template>
    <div>
        <p>Somos a {{ empresa }}</p>
        <p>Iniciamos em {{ date }}</p>
        <MultpleEvents />
        <Reuse />
    </div>
</template>

<script>
import MultpleEvents from './MultpleEvents.vue'
import Reuse from './ReuseComp.vue'

export default {
    name: 'FirstComp',
    components: {
        MultpleEvents,
        Reuse
    },
    data(){
        return {
            empresa: 'byGood Produtora Digital',
            date: '2020'
        }
    }
}
</script>