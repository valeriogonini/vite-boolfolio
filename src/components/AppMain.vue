<template>
    <div>
        Eccoci
    </div>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            projects: []
        }
    },
    methods: {
        fetchProject() {
            axios.get('http://127.0.0.1:8000/api/projects')
                .then((res) => {
                    console.log(res.data.results.data)

                })
        }

    },
    created() {
        this.fetchProject()
    },
}
</script>

<style lang="scss" scoped></style>