<template>
  <NuxtLink :to="`/products/${card.id}`" class="card">
    <img :src="require(`@/assets/img/${card.image}`)" :alt="card.title" class="image">
    <h3 class="header">{{ card.title }}</h3>
    <p class="snippet">{{ card.snippet }}</p>
  </NuxtLink>
</template>

<script>
export default {
  props: ['card']

}
</script>

<style scoped>
.card {
    width: 31.5%;
    height: 25rem;
    border: none;
    overflow: hidden;
    padding: 0;
    cursor: pointer;
}
.card:hover {
  text-decoration: none;
}
.image {
    height: 60%;
    border-radius: 0.5rem;
}
.header {
    color: #333;
    font-size: 1.15rem;
    margin-top: 0.4rem;
}
.header:hover {
  color: green;
  text-decoration: none;
}
.snippet {
    color: grey;
    font-size: 0.9rem;
}
@media (max-width: 750px) {
  .card {
    width: 90%;
    height: 22rem;
  }
}
</style>