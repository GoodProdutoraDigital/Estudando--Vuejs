<template>
  <div>
    <Header :logged="true"/>
    <h1 class="p-pai">Seja bem vindo ao {{ title }}</h1>
    <FirstCompVue />
    <LifeCycle />
    <Registro />
  </div>
</template>

<script>
import FirstCompVue from './components/FirstComp.vue';
import LifeCycle from './components/LifeCycle.vue';
import Registro from './components/Registro.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
    FirstCompVue,
    LifeCycle,
    Registro
  },
  data() {
    return {
      title: 'VueJS'
    }
  }
}
</script>

<style>
/* Global style */
body{
  background-color: #333;
  color: #fff
}
a{
  color: brown;
}
.img-size{  
  width: 100px;
}
</style>