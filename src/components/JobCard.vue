<script setup>

</script>

<template>
    <div class="job-card">
        <!-- Top row: logo + company info + badge -->
        <div class="top-row">
            <div class="job-info">
                <img src="../assets/logo.png" alt="Google" class="logo">
                <div class="text-info">
                    <div class="company-name">Google</div>
                    <div class="date">2 days ago</div>
                </div>
            </div>
            <div class="badge">Part Time</div>
        </div>

        <!-- Bottom content: job title, location, description -->
        <div class="bottom-content">
            <div class="job-title">Frontend Developer</div>
            <div class="location"><i class="fa-solid fa-location-dot"></i> Remote</div>
            <h3 class="description">Work on amazing Vue.js projects with our team!
            </h3>
        </div>
    </div>
</template>



<style>
.job-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 20px;
    width: 80%;
    display: flex;
    flex-direction: column;
    /* stack top and bottom sections */
    gap: 10px;
    /* space between top and bottom */
    margin: 1em auto;
}

.top-row {
    display: flex;
    justify-content: space-between;
    /* badge on right */
    align-items: center;
}

.job-info {
    display: flex;
    align-items: center;
}

.logo {
    width: 40px;
    height: 40px;
    margin-right: 10px;
}

.text-info {
    display: flex;
    flex-direction: column;
}

.company-name {
    font-weight: bold;
}

.date {
    font-size: 0.85rem;
    color: gray;
}

.badge {
    background-color: #e0f2fe;
    color: #0284c7;
    padding: 2px 8px;
    border-radius: 12px;
    font-size: 0.8rem;
    font-weight: 500;
}

.bottom-content {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.job-title {
    font-weight: bold;
}

.location {
    font-size: 0.85rem;
    color: gray;
}

.description {
    font-size: 0.9rem;
    color: #6b7280;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    /* number of lines to show */
    -webkit-box-orient: vertical;
}

img {
    border-radius: 5px;
}
</style>