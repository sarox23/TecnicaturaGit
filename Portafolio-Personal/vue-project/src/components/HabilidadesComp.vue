<script setup>
import js from '/src/components/icons/js.svg';
import python from '/src/components/icons/python.svg';
import html from '/src/components/icons/html-css.svg';
import java from '/src/components/icons/java.svg';

import { ref } from 'vue';

const habilidades = ref([
    {
        id: 1, nombre: 'Lenguajes de Programación', habilidades: [
            { id: 1, nombre: 'JavaScript', nivel: 'Basico', icono: js },
            { id: 2, nombre: 'Python', nivel: 'Intermedio', icono: python },
            { id: 3, nombre: 'HTML/CSS', nivel: 'Basico', icono: html },
            { id: 4, nombre: 'Java', nivel: 'Basico', icono: java },
        ]
    },

]);

</script>


<template>
    <div class="skills-contenedor">
        <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
            <h3>{{ habilidad.nombre }}</h3>
            <ul class="skills">
                <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
                    <img :src="habilidad.icono" :alt="habilidad.nombre">
                    <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
                </li>
            </ul>
        </div>
    </div>


</template>

<style scoped>
.skills-contenedor {
    padding: 2rem;
    background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B6);

}

.skills-categoria {
    margin-bottom: 20px;
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: aliceblue;
    font-size: 1.5em;
    font-weight: bold;
}

.skills {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3em;
    border-radius: 8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span {
    font-size: 1em;
    color: #333;
}

.skill:hover {
    font-size: 1.3em;
    transition: 2s ease;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}
</style>