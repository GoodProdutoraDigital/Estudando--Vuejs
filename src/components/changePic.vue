<template>
  <div>
    <button @click="$emit('change')">Mudar imagem</button>
  </div>
</template>

<script>
export default {
    name: 'changePic',
    emits: ['change']
}
</script>