<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';
const intereses = ref([
    'Quiero seguir aprendiendo y mejorando en programacion, es lo que me gusta y mientras mas aprendo mas me apasiona.',
    'Deportes al Aire Libre: He hecho todo tipo de deportes, pero mas que nada me gusta el voley o boxeo, tambien me gusta ver la formula 1 o futbol.',
    'Programacion: Me parece todo muy interesante cuando voy entiendiendo un lenguaje de programacion, aunque al principio me frusta por no entender bien',
    'Videojuegos: Mi hobbie favorito es jugar videojuegos, es divertido cuando estoy con amigos y me rio bastante.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>