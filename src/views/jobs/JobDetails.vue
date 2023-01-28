<template>
        <div class="jobs">
            <h1>Job Details</h1>
            <p>The job ID is: {{ id }}</p>
        </div>
</template>

<script>

export default {
    name: 'JobDetails',
    props: ["id"],
    components: {  },
    data() {
        return {

        }
    }
}
</script>
