<template>
  <h1>Hello App!</h1>
  <p>
    <strong>Current route path:</strong> {{ $route.fullPath }}
  </p>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/portfolio">Portfolio</RouterLink>
    <RouterLink to="/contact">Contatti</RouterLink>

  </nav>
  <main>
    <RouterView />
  </main>
</template>
<script>
import AppMain from './components/AppMain.vue';
export default {
  components: {
    AppMain

  }

}
</script>

<style lang="scss" scoped></style>
