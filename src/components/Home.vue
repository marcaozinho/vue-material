<template>
  <div class="home">
    <ComponentTop/>
    <h3>Home</h3>
    <img src="../assets/logo.png" align="center">
    <component-card></component-card>
  </div>
</template>

<script>
import ComponentTop from './Top.vue'
import ComponentCard from './Card.vue'
export default {
  components: {
    ComponentTop, ComponentCard
  }
}
</script>

<style scoped>
</style>
