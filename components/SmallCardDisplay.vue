<template>
  <div class="container">
    <h3 class="header">{{ cardsSection.title }}</h3>
    <div class="card-container">
      <SmallCard 
        v-for="card in cardsSection.cards"
        :key="card.id"
        :card = "card"
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
.container {
  padding: 2rem 0
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}
.card-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}

@media (max-width: 1000px) {
  .card-container {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 750px) {
  .card-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 420px) {
  .card-container {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>