<script setup>
const produtos = [
    {
        id: 1,
        imagem: 'https://via.placeholder.com/300x200.png?text=Produto+1',
        titulo: 'Produto 1',
        descricao: 'Descrição breve do produto 1.',
        delay: 100,
    },
    {
        id: 2,
        imagem: 'https://via.placeholder.com/300x200.png?text=Produto+2',
        titulo: 'Produto 2',
        descricao: 'Descrição breve do produto 2.',
        delay: 200,
    },
    {
        id: 3,
        imagem: 'https://via.placeholder.com/300x200.png?text=Produto+3',
        titulo: 'Produto 3',
        descricao: 'Descrição breve do produto 3.',
        delay: 300,
    },
    // Adicione mais produtos conforme necessário
];
</script>


<template>
    <section class="py-16">
        <h2 class="text-3xl font-bold text-center mb-12" data-aos="fade-up">Produtos em Destaque</h2>
        <div class="max-w-6xl mx-auto grid gap-8 grid-cols-1 md:grid-cols-3">
            <div v-for="(produto, index) in produtos" :key="produto.id" class="max-w-xs mx-auto" data-aos="fade-up"
                :data-aos-delay="produto.delay">
                <img :src="produto.imagem" :alt="produto.titulo" class="mb-4">
                <h3 class="text-xl font-semibold">{{ produto.titulo }}</h3>
                <p class="mt-2 text-gray-600">{{ produto.descricao }}</p>
            </div>
        </div>
    </section>
</template>

