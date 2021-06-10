<template>
  <section class="barra">
      <img class="logo_header" src="../assets/spotify.png" alt="Logo spotify">
      <select name="" id="" v-model="selected" @change="selectedValue">
          <option value="">Seleziona il genere</option>
          <option value="pop">Pop</option>
          <option value="rock">Rock</option>
          <option value="jazz">Jazz</option>
          <option value="metal">Metal</option>
      </select>
  </section>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style>
    .barra{
        background-color: #2E3A46;
        height: 65px;
    }

    .logo_header{
        width: 45px;
        margin-left: 10px;
        margin-top: 10px;
    }
</style>