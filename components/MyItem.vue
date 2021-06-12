<template>
  <div class="d-flex my-3">
    <img :src="require(`@/assets/img/${item.image}`)" alt="">
    <div class="pl-5">
      <h4>{{item.title}}</h4>
      <p class="text-secondary">{{item.description}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['item']
}
</script>

<style scoped>
  img {
    width: 17.5rem;
    border-radius: 0.5rem;
  }

</style>