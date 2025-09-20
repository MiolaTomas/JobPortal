<script setup>

</script>

<template>
    <div class="hero">
        <div class="hero-content">
            <h1>Welcome to My App</h1>
            <p>Learning Vue with a beautiful hero section ✨</p>
            <button>Get Started</button>
        </div>

    </div>
</template>

<style>
body {
    padding-top: 4em;
    /* same as header height */
}

.search-bar {
    display: flex;
    justify-content: center;
    align-items: center;
    background: white;
    border-radius: 2rem;
    margin-top: 1em;
    overflow: hidden;
    max-width: 500px;
    width: 100%;
}


.hero {
    width: 90%;
    height: calc(97vh - 4em);
    background-color: #1e483e;
    background: linear-gradient(135deg,
            #7be4c8 0%,
            #42b883 35%,
            #35495e 90%);

    /* soft gradient */
    border-radius: 1.5rem;
    /* adjust this for more/less roundness */
    overflow: hidden;
    margin: 0 auto;
    /* ensures child elements like waves don't "leak" outside */
}

.hero {
    width: 90%;
    height: calc(97vh - 4em);
    background: linear-gradient(135deg,
            #7be4c8 0%,
            #42b883 35%,
            #35495e 90%);
    border-radius: 1.5rem;
    overflow: hidden;

    display: flex;
    /* enable flexbox */
    justify-content: center;
    /* center horizontally */
    align-items: center;
    /* center vertically */
    text-align: center;
    color: white;
    padding: 2rem;
}

.hero-content h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.hero-content p {
    font-size: 1.25rem;
    margin-bottom: 2rem;
}

.hero-content button {
    background: white;
    color: #35495e;
    border: none;
    padding: 0.75rem 1.5rem;
    border-radius: 0.75rem;
    font-size: 1rem;
    cursor: pointer;
    transition: background 0.3s ease;
}

.hero-content button:hover {
    background: #f0f0f0;
}
</style>