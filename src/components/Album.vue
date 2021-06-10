<template>
  <div class="album">
      <div class="schermo">
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
    /* display: flex;
    justify-content: center; */
    float: left;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    padding: 24px;
    }

  .immagine_copertina{
    width: 90px;
    height: auto;
    flex-wrap: wrap;
  }

  .schermo{
    float: left;
  }

  .schermo h2{
    color: white;
  }

  .schermo h3, h4{
    color: lightslategrey;
  }
</style>