<template>
        <div class="jobs">
            <h1>Jobs</h1>
            <div v-for="job in jobs" :key="job">
                <router-link :to="{ name: 'job_details', params: { id: job.id } }">
                    <h2>{{ job.title }}</h2>
                </router-link>
            </div>
        </div>
</template>

<script>

export default {
    name: 'JobsView',
    components: {  },
    data() {
        return {
            jobs: [
                { id : 0, title: 'UX Developer', details: 'description' },
                { id : 1, title: 'Web Developer', details: 'description' },
                { id : 2, title: 'Vue Developer', details: 'description' }
            ]
        }
    }
}
</script>

<style>
    .jobs h2 {
        background: #f4f4f4;
        padding: 20px;
        border-radius: 10px;
        margin: 10px auto;
        max-width: 600px;
        cursor: pointer;
        color: #444;
    }

    .jobs h2:hover {
        background: #ddd;
    }

    .jobs a {
        text-decoration: none;
    }
</style>
