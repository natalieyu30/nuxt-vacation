<template>
  <NuxtLink :to="`/products/${card.id}`">
    <div class="card-container">
      <img :src="require(`@/assets/img/${card.image}`)" :alt="card.image" class="image">
    </div>
  </NuxtLink>
</template>

<script>
export default {
  props: ['card']
}
</script>

<style scoped>
/* .card-container {
    width: 24%;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    height: 12.5rem;
    border-radius: 0.5rem;
    overflow: hidden;
    margin-bottom: 1.5rem;
    cursor: pointer;
} */
.image {
  width: 100%;
  height: 12.5rem;
}
</style>