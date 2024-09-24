<template>
    <section class="py-16">
        <h2 class="text-3xl font-bold text-center mb-12" data-aos="fade-up">Últimas do Blog</h2>
        <div class="max-w-5xl mx-auto grid gap-8 grid-cols-1 md:grid-cols-3">
            <div v-for="(artigo, index) in artigos" :key="artigo.id" class="bg-gray-100 p-6 rounded" data-aos="fade-up"
                :data-aos-delay="100 * index">
                <img :src="artigo.imagem" :alt="artigo.titulo" class="mb-4 rounded">
                <h3 class="font-semibold text-xl mb-2">{{ artigo.titulo }}</h3>
                <p class="text-gray-600">{{ artigo.descricao }}</p>
            </div>
        </div>
    </section>
</template>

<script setup>
const artigos = [
    {
        id: 1,
        imagem: 'https://via.placeholder.com/400x250.png?text=Artigo+1',
        titulo: 'Título do Artigo 1',
        descricao: 'Resumo breve do artigo 1 para despertar interesse.',
    },
    {
        id: 2,
        imagem: 'https://via.placeholder.com/400x250.png?text=Artigo+2',
        titulo: 'Título do Artigo 2',
        descricao: 'Resumo breve do artigo 2 para despertar interesse.',
    },
    {
        id: 3,
        imagem: 'https://via.placeholder.com/400x250.png?text=Artigo+3',
        titulo: 'Título do Artigo 3',
        descricao: 'Resumo breve do artigo 3 para despertar interesse.',
    },
    // Adicione mais artigos conforme necessário
];
</script>

<style scoped>
/* Estilos específicos, se necessário */
</style>
