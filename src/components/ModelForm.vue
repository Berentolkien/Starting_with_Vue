<template>
    <form>
        <input type="text" v-model="inputText">
        <input type="checkbox" v-model="agree"/> Acepto los terminos y condiciones
        <select>
            <option value="Spain">Spain</option>
            <option value="UK">UK</option>
            <option value="France">France</option>
        </select>
    </form>
    <h3>{{ inputText }}</h3>

</template>

<script lang="ts" setup>
    import {Ref, ref } from 'vue'
    let inputText:Ref<string> = ref('')
    let agree = ref(true)
</script>

<style scoped>
</style>