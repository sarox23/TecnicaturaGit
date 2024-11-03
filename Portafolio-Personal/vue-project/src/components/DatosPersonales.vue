<script setup>
const title = "Martiniano Zallocco";
const descripcion = "estudiante de la Tecnicatura en Programacion";
const residencia = "San Rafael, Mendoza, Argentina";
const presentacion = "Hola, bienvenido a mi portafolio de proyecto, soy un estudiante de la tecnicatura en Progamacion en la UTN.";
const redessociales =[
    { id: 1, name: "linkedin", src: "/src/assets/linkedin_icon.svg", url: "https://www.linkedin.com" },
    { id: 2, name: "instagram", src: "/src/assets/instagram_icon.svg", url: "https://www.instagram.com" },
    { id: 3, name: "github", src: "/src/assets/github_icon.svg", url: "https://github.com" },
    { id: 4, name: "curriculum", src: "/src/assets/cv_resume_icon.svg", url: "f" },
];
const telefono = "+54 9 2604597616";
</script>

<template>
<section class="datos-personales">
    <div class="card">
        <h1>{{ tittle }}</h1>
        <h2>{{ descripcion }}</h2>
        <p>{{ presentacion }}</p>
        <u1 class="conteiner-list">
            <li v-for="red in redessociales" :key="red.id"></li>
            <a href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
        </u1>
        <h3>Contacto: +54 9 2604597616</h3>
        <h4>{{ residencia }}</h4>
    </div>
</section>
</template>

<style scoped>
.conteiner-list {
    list-style-type: none;
    padding: 0;
}
.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}
.icon-redsocial:hover {
    background-color: rgb(28, 41, 52);
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}
h1 {
    font-size: 1.2rem;
    font-weight: 600;
}
</style>