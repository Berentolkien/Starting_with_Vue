<template>
    <ul>
        <li v-for="country in countries" v-bind:key="country.code">{{ country.name }}</li>
    </ul>
</template>

<script lang="ts" setup>
import { Ref, ref } from 'vue'
interface ICountry {
    code:string,
    name: string
}
let countries: Ref<Array<ICountry>> = ref([
    {
        code: 'es',
        name: 'Spain'
    },
    {
        code: 'en',
        name: 'uk'
    },
    {
        code: 'fr',
        name: 'france'
    },
    {
        code: 'it',
        name: 'Italy'
    },
    {
        code: 'pt',
        name: 'Portugal'
    }
])
</script>

<style scoped>
li {
  color: green;
}

</style>