<script setup>
</script>

<template>
    <h1 class="infinite-title">Companies we have worked with</h1>
    <div class="carousel">
        <!-- First group -->
        <div class="group">
            <div class="card"><i class="fa-brands fa-instagram fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-microsoft fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-amazon fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-apple fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-linkedin fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-steam fa-5x"></i></div>
        </div>

        <!-- Second group (clone of first, for seamless loop) -->
        <div class="group" aria-hidden="true">
            <div class="card"><i class="fa-brands fa-instagram fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-microsoft fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-amazon fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-apple fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-linkedin fa-5x"></i></div>
            <div class="card"><i class="fa-brands fa-steam fa-5x"></i></div>
        </div>
    </div>
</template>

<style>
i {
    color: lightgray;
}

.infinite-title {
    color: var(--main-text);
    font-size: 2em;
    margin: 1em auto;
    text-align: center;
}

.carousel {
    width: 80%;
    margin: 4em auto;
    display: flex;
    overflow: hidden;
    /* hide scrollbar */
    position: relative;
}

.group {
    display: flex;
    animation: scroll 15s linear infinite;
}

.card {
    flex: 0 0 auto;
    /* don’t shrink */
    padding-right: 6em;
}

@keyframes scroll {
    from {
        transform: translateX(0);
    }

    to {
        transform: translateX(-100%);
    }
}
</style>
