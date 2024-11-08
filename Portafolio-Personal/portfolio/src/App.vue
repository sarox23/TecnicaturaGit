<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionComp from "./components/EducacionComp.vue"
import ExperienciaComp from "./components/ExperienciaComp.vue"
import ProyectoComp from "./components/ProyectoComp.vue"
import HabilidadesComp from "./components/HabilidadesComp.vue"
import InteresesComp from "./components/InteresesComp.vue"


</script>

<template>
  <header>
    <!--barra de navegacion-->
    <NavBar />
    <!--componente datos personales-->
    <DatosPersonales/>
</header>
<main>
    <!--el estilo css de section se encuentra en base.css-->
    <section id="educacion"><h2>Educación - Cursos</h2> <EducacionComp /> </section>
    <section id="experiencia"><h2>Experiencia</h2> <ExperienciaComp /> </section>
    <section id="proyectos"><h2>Proyectos</h2> <ProyectoComp /> </section>
    <section id="habilidades"><h2>Habilidades</h2> <HabilidadesComp /> </section>
    <section id="intereses"><h2>Intereses</h2> <InteresesComp /> </section>
</main>
</template>
<style scoped>
</style>

