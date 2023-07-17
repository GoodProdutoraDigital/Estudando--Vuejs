<template>
    <div>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Projetos</a></li>
            <li><a href="#">Contato</a></li>
            <li v-if="logged"><a href="#">Meu Perfil</a></li>
        </ul>     
    </div>
</template>

<script>
export default {
    name: 'Header',
    props: ['logged']
}
</script>

<style scoped>
ul{
    list-style: none;
    display: flex;
    background: #999;
    border: 5px;
    border-radius: 7px;
}
li{
    margin-right: 10px;
}
a{
    color: #fff;
    text-decoration: none;
    transition: .5s;
}
a:hover{
    color: brown;
}
</style>