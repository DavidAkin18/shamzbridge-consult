<template>
  <div class="Landing-page">
    <Navbar />
    <div class="content">
      <HeroSection />
      <About />
      <ServiceSection />
    </div>
    <Footer />
  </div>
</template>

<script>
import About from './About.vue';
import Footer from './Footer.vue';
import HeroSection from './HeroSection.vue';
import Navbar from './Navbar.vue';
import ServiceSection from './ServiceSection.vue';

export default {
    components:{
        Navbar,
        About,
        Footer,
        HeroSection,
        ServiceSection
    }
}
</script>

<style>
html, body {
  height: 100%; 
  margin: 0;    
}

.Landing-page {
  display: flex;
  flex-direction: column;
  min-height: 100vh; 
}

.content {
  flex: 1; 
}
</style>