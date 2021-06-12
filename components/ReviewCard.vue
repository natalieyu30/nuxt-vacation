<template>
  <div class="review-card">
    <div class="image-container">
      <img :src="review.picture.large" alt="">
    </div>
    <div class="text-container">
      <h6>{{review.login.username}}</h6>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum quidem ex, eligendi molestias dolores accusantium labore repellendus quod quisquam! Dolorum asperiores omnis quae, ipsa consectetur commodi tenetur neque impedit veniam.</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['review'],
}
</script>

<style scoped>
.review-card {
  margin-top: 1.5rem;
  height: 4rem;
  display: flex;
}
.text-container {
  margin-left: 2rem;
}
img {
  width: 4rem;
  height: 4rem;
  border-radius: 100%;
}
p {
  color: grey;
  font-size: 0.8rem;
}
@media (max-width: 750px) {
  .review-card {
    height: 6.5rem;
  }
    }
@media (max-width: 420px) {
  .review-card {
    margin-top: 1rem;
    height: 12rem;
    flex-direction: column;
  }
  .text-container {
    margin-left: 1rem;
  }
  img {
    width: 2.5rem;
    height: 2.5rem;
  }
  p {
    color: grey;
    font-size: 0.8rem;
  }
}
</style>