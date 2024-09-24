<template>
  <div>
    <Navbar />
    <HeroSection />
    <FeaturedProducts />
    <Testimonials />
    <Newsletter />
    <Blog />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue';
import HeroSection from './components/HeroSection.vue';
import FeaturedProducts from './components/FeaturedProducts.vue';
import Testimonials from './components/Testimonials.vue';
import Newsletter from './components/Newsletter.vue';
import Blog from './components/Blog.vue';
import Footer from './components/Footer.vue';
</script>

<style>
/* Estilos globais */
body {
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
}
</style>
