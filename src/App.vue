<script setup>

import Container from "./components/Container.vue";
import HeroSection from "./components/HeroSection.vue";
import Projects from "./components/Projects.vue";
import Competence from "./components/Competence.vue";
import Contact from "./components/Contact.vue";
import Apropos from "./components/Apropos.vue";

</script>

<template>
  <Container>
    <HeroSection/>
    <Apropos/>
    <Projects/>
    <Competence/>
    <Contact/>
  </Container>
</template>

<style scoped></style>
