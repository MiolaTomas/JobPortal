<script setup>
import { ref } from 'vue';

const menuOpen = ref(false);

function toggleMenu() {
    menuOpen.value = !menuOpen.value;
}
</script>

<template>
    <div class="header">
        <div class="navbar">
            <div class="logo">
                <img src="../assets//logo1.png" alt="">
                <span>VueBoard</span>
            </div>

            <div class="nav-links" :class="{ active: menuOpen }">
                <ul>
                    <li><a href=" #">Inicio</a></li>
                    <li><a href="#">Trabajos</a></li>
                    <li><a href="#">Sobre Nosotros</a></li>
                    <li><button>Post a job</button></li>
                </ul>
            </div>
            <button class="hamburger" @click="toggleMenu">
                &#9776; <!-- simple hamburger icon -->
            </button>
        </div>

    </div>
</template>

<style>
.header {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background-color: white;
    align-items: center;
}

.navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 80%;
    margin: 0 auto;
    padding: 1em 0;
}

.logo {
    display: flex;
    align-items: center;
    gap: 1em;
}

.logo img {
    width: 3em;
}

.logo span {
    font-style: normal;
    color: var(--main-text);
    font-size: 1.2em;
    font-weight: bold;
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 1em;
}

.nav-links ul {
    display: flex;
    gap: 1em;
    list-style: none;
    align-items: center;
}


.nav-links a {
    text-decoration: none;
    color: var(--main-text);
    font-weight: 600;
}

.nav-links button {
    background-color: var(--cta-green);
    color: white;
    padding: 1em 2em;
    border: none;
    border-radius: .2em;
    cursor: pointer;
    font-weight: 600;
    font-size: .9em;
}

.nav-links button:hover {
    background-color: var(--cta-green-hover);
}

.nav-links a:hover {
    text-decoration: none;
    color: var(--cta-green);
}


.hamburger {
    display: none;
    font-size: 1.5em;
    background: none;
    border: none;
    cursor: pointer;
}

@media (max-width: 640px) {

    .hamburger {
        display: flex;
        font-size: 1.5em;
        background: none;
        border: none;
        cursor: pointer;
        color: var(--font-black-before-hover);
    }

    .hamburger:hover {
        color: var(--main-black);
    }

    .nav-links {
        flex-direction: column;
        position: fixed;
        left: 0;
        top: 4em;
        width: 100%;
        height: 100vh;
        background-color: white;
    }

    .nav-links ul {
        flex-direction: column;
        gap: 1em;
        font-size: 1.5em;
        margin-top: 1em;
    }

    .nav-links.active {
        display: none;
        /* show when active */
    }

}
</style>