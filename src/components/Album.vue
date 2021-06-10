<template>
  <div class="Album">
      <div>
        <img class="immagine_copertina" :src="item.poster" :alt="item.title">
        <h2>{{item.title}}</h2>
        <h3>{{item.author}}</h3>
        <h4>{{item.year}}</h4>
      </div>
    </div>
</template>

<script>
export default {
    name: "Album", 
    props: ["item"]
}
</script>

<style>
  .album{ 
    display: inline-block;
  }

  .immagine_copertina{
    width: 90px;
    height: 100%;
    flex-direction: row;
    display: flex;
    flex-wrap: wrap;
  }
</style>