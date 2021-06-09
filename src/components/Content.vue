<template>
  <main class="contenuto">
      <Albums />
  </main>
</template>

<script>
import Albums from './Albums.vue'
export default {
    name: "Content",
    components: {
        Albums
    }
}
</script>

<style>
    .contenuto{
        height: calc(100vh - 65px);
        background-color: #1E2D3B;
    }
</style>