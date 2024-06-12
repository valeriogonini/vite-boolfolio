<template>
    <h1>I miei progetti</h1>
    <ul v-for="project in projects">
        <li>
            <h2>{{ project.nome_progetto }}</h2>
            <h4> Slug: {{ project.slug }}</h4>
            <p> Descrizione :{{ project.descrizione_progetto }}</p>
            <p>link github: {{ project.link_github_progetto }}</p>
        </li>
    </ul>
</template>

<script>
import axios from 'axios'

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
                    console.log(res.data.projects);
                    this.projects = res.data.projects

                })
        }

    },
    created() {
        this.fetchProject()
    },
}
</script>

<style lang="scss" scoped></style>