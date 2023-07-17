<template>
    <div>
        <!-- Sintax v-bind resumida por { : } -->
        <img class="img-size" :src="avatar" :alt="desc">
        <changePic @change="mudarImg" />
    </div>
</template>

<script>
import changePic from '../changePic.vue';

export default {
    name: 'Pic',
    components: {
        changePic
    },
    data() {
        return {
            avatar: '/img/image-example.png',
            desc: 'Jefferson'
        }
    },
    methods:{
        mudarImg(){
            this.avatar = './img/avatar.png'
        }
    }
}
</script>