<template>
  <div class="large-card">
    <h4 class="header">{{ cardsSection.title }}</h4>
    <p class="snippet">{{ cardsSection.snippet }}.</p>
    <div class="cards-container">
      <LargeCard
        v-for="card in cardsSection.cards"
        :key="card.id" 
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ['cardsSection']

}
</script>

<style scoped>
.large-card {
  margin-top: 1.5rem;
  display: block;
}
.header {
    font-weight: 700;
    font-size: 1.5rem;
}
.snippet {
    color: grey;
    margin-bottom: 1.5rem;
}
.cards-container {
    display: flex;
    justify-content: space-between;
}
@media (max-width: 750px) {
  .cards-container {
    flex-direction: column;
    align-items: center;
  }
}
@media (max-width: 420px) {
  /* .large-card {
    margin-top: 8rem;
  } */
}
</style>