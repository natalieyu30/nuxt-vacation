<template>
  <div>
    <div v-if="product" class="container py-5">
      <div class="hero-container">
        <img :src="require(`@/assets/img/${product.image}`)" alt="" class="image">
        <div class="info-box">
          <h1>{{ product.title }}</h1>
          <p class="snippet">{{ product.snippet }}</p>
          <ReserveModal :product="product" />
        </div>
      </div>
      <div class="whats-included-container">
        <div class="included-container">
          <h6>Best Experience</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium esse aperiam commodi adipisci numquam asperiores.</p>
        </div>
        <div class="included-container">
          <h6>Relax and Refresh</h6>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos officiis deserunt nostrum!</p>
        </div>
        <div class="included-container">
          <h6>Explore Around</h6>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dicta vitae assumenda et natus dolor repellat, cumque debitis.</p>
        </div>
      </div>
      <div class="description-container">
        <p>{{ product.description }}</p>
      </div>
      <Reviews />
    </div>
    <div v-else class="container">
      <PageNotFound />
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import Reviews from '../../components/Reviews.vue'

export default {
  components: { Reviews },
  computed: {
    product() {
      return this.$store.getters.getProductById(this.$route.params.id)
    }
  }
}
</script>

<style scoped>
    .hero-container {
        display: flex;
        justify-content: space-between;
    }
    .image {
        width: 59%;
        height: 25rem;
    }
    .info-box {
        width: 39%;
        background-color: rgba(207, 201, 201, 0.322);
        padding: 1rem;
        border-radius: 0.5rem;
    }
    .whats-included-container {
        border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
    }
    .description-container {
        border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
        padding-bottom: 2rem;
        margin-bottom: 2rem;
    }
    .included-container {
        margin-top: 1.2rem;
    }
    h1 {
        font-size: 1.75rem;
    }
    h6 {
        font-size: 1.2rem;
        font-weight: 700;
        color: green;
    }
    p {
        color: grey;
        font-size: 0.9rem;
    }
    .snippet {
        color: rgba(0, 0, 0, 0.774);
        margin-top: 1rem;
    }
    button {
        width: 100%;
        border: none;
        padding: 0.5rem;
        color: white;
        font-weight: 700;
        padding: 1rem 4rem;
        border-radius: 100rem;
        background-color: rgb(231, 81, 43);
        color: white;
        font-weight: 700;
        transition: 0.5s;
    }
    .description-container {
        margin-top: 2rem;
        color: grey
    }
    .padding {
        padding: 10rem 0
    }
    @media (max-width: 420px) {
      .hero-container {
        flex-direction: column;
      }
      .image {
        width: 100%;
        height: 100%;
      }
      .info-box {
          width: 100%;
      }
    }
</style>