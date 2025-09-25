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
                <img src="../assets//vue.png" alt="">
                <span>JsJobs</span>
            </div>

            <div class="nav-links" :class="{ active: menuOpen }">
                <ul>
                    <li><a href=" #">Home</a></li>
                    <li><a href="#">Products</a></li>
                    <li><a href="#">Contacts</a></li>
                    <button>Post a job</button>
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
    height: 4em;
    position: fixed;
    top: 0;
    left: 0;
    background-color: white;
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
    width: 2em;
    height: 1.7em;
}

.logo span {
    font-style: normal;
    color: var(--main-black);
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
}


.nav-links a {
    text-decoration: none;
    color: var(--font-black-before-hover);
    font-weight: 600;
}

.nav-links a:hover {
    text-decoration: none;
    color: var(--main-black);
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
        align-items: flex-start;
        background-color: white;
    }

    .nav-links ul {
        flex-direction: column;
        gap: 1em;
        margin-top: .5em;
        margin-left: 3em;
    }

    .nav-links.active {
        display: none;
        /* show when active */
    }

    .nav-links button {}
}
</style>