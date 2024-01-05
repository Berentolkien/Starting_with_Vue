<template>
    <div><h1>Hola Mundo</h1></div>
</template>

<script lang="ts" setup>
import { onMounted, onUpdated } from 'vue'

onMounted(() => {
    console.log("mounted")
}) 

onUpdated(() => {
    console.log("updated")
})
</script>

<style scoped>
</style>