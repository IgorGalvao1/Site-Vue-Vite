<template>
    <div class="max-w-md mx-auto mt-10 p-4">
        <h1 class="text-3xl font-bold mb-6 text-center">Lista de Tarefas</h1>
        <div class="flex mb-4">
            <input v-model="novaTarefa" @keyup.enter="adicionarTarefa"
                class="flex-grow border rounded-l px-3 py-2 focus:outline-none" type="text"
                placeholder="Adicionar nova tarefa" />
            <button @click="adicionarTarefa" class="bg-blue-600 text-white px-4 py-2 rounded-r hover:bg-blue-700">
                Adicionar
            </button>
        </div>
        <ul>
            <li v-for="(tarefa, index) in tarefas" :key="index"
                class="flex justify-between items-center bg-gray-100 px-4 py-2 mb-2 rounded">
                <span>{{ tarefa }}</span>
                <button @click="removerTarefa(index)" class="text-red-500 hover:text-red-700">
                    Remover
                </button>
            </li>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const tarefas = ref([]);
const novaTarefa = ref('');

function adicionarTarefa() {
    if (novaTarefa.value.trim() !== '') {
        tarefas.value.push(novaTarefa.value.trim());
        novaTarefa.value = '';
    }
}

function removerTarefa(index) {
    tarefas.value.splice(index, 1);
}
</script>

<style scoped>
/* Estilos específicos do componente, se necessário */
</style>
