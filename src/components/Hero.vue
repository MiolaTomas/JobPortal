<script setup>

</script>

<template>
    <div class="hero">
        <div class="hero-content">
            <h1>Join us & <span>Explore</span></h1>
            <h1><span>Thousands</span> of Jobs</h1>
            <p>Find Jobs, Employment & Career Opportunities. Some of the companies we've helped recruit excellent
                applicants over the years.</p>
            <div class="hero-search-bar">
                <div class="keyword">
                    <i class="fa-solid fa-briefcase"></i>
                    <input type="text" placeholder="Search keyword">
                </div>
                <button>Search</button>
            </div>
        </div>
    </div>
</template>

<style>
body {
    padding-top: 4em;
    /* same as header height */
}

h1 {
    color: #0f172b;
    font-size: 3em;
}

span {
    color: #009966;
}

p {
    color: #90a1b9;
    width: 80%;
    margin: 1em auto;
}

.hero {
    width: 100%;
    height: calc(97vh - 4em);
    background-color: #f2faf7;

    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.hero-search-bar {
    width: 80%;
    background-color: white;
    margin: 1.5em auto;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    border: 1px solid #e5e7eb;
    border-radius: .2em;
    display: flex;
    padding: .5em;
    justify-content: space-between;
}

.keyword {
    padding: .8em;
    display: flex;
    width: 100%;
}

.hero-search-bar button {
    background-color: #009966;
    border: none;
    color: white;
    cursor: pointer;
    padding: 0 2em;
    border-radius: .2em;
}

.hero-search-bar button:hover {
    background-color: #008357;
    border: none;
    color: white;
    cursor: pointer;
    padding: 0 2em;
    border-radius: .2em;
}

.keyword input {
    all: unset;
    all: unset;
    display: inline-block;
    width: 100%;
    color: #90a1b9;
}
</style>