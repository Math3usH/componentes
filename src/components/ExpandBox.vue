<script setup>
import { ref, computed } from 'vue';

// const props = defineProps(['title', "content"])
defineProps({
    title: {
        type: String,
        required: true
    },
    content: {
        type: String,
        default: "Valor padrão do texto da caixa..."
    },
    quantity: {
        type: Number,
        default: 10
    }
})

const showContent = ref(false)
const textButton = computed(() => (showContent.value ? 'Esconder' : 'Mostrar'))
</script>

<template>
    <div>
        <button @click="showContent = !showContent">{{ textButton }}</button>
        <div v-if="showContent" class="Expand-box">
            <h1>{{ title }}</h1>
            <p>{{ content }}</p>
            <p>Quantidade: {{ quantity }}</p>
        </div>
    </div>
</template>

<style scoped>
.Expand-box {
    height: 100%;
    padding: 20px;
    border: 1px solid black;
    box-shadow: 2px 2px 3px 3px gray;
    border-radius: 10px;
}
</style>