<template>
  <div>
    <h1>Page Not Found</h1>
    <img :src="require('@/assets/img/together.png')" alt="">
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  div{
    margin-top: 5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50rem;
  }

  h1 {
    font-size: 5rem;
  }

  img {
    width: 60%;
    margin: 0 auto;
  }
</style>