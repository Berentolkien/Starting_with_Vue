<template>
    <div class="post">
        <h3>{{ props.title }}</h3>
        <p>{{ props.content }}</p>
        <input type="text" v-model="message"/>
        <button @click="handleClick">Di hola</button>
    </div>
</template>

<script lang="ts">
import { defineComponent, handleError, Ref, ref } from 'vue';
export default defineComponent({
    name: 'PostDetail',
    props: {
        title : {
            type: String,
            required: true
        },
        content: {
            type: String,
            require: false,
            default: "Este post no tiene contenido"
        }
    },
    emits: ["sayHi"],
    setup(props, {emit}) {
        const handleClick = () => {
            emit("sayHi", message.value)
        }
        let message:Ref<string> = ref("")
        return {props, message, handleClick}
    }
})
</script>

<style scoped>
.post {
    width: 200px;
    height: 300px;
    background-color: antiquewhite;
    border-radius: 10px;
    margin: 10px;
    padding: 10px;
}

</style>