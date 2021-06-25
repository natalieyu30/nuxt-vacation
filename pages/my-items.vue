<template>
  <div class="container">
    <MyItem 
      v-for="item in myRentals"
      :key="item.id"
      :item="item"
    />
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  layout: 'default',
  computed: {
    ...mapState(['myRentals'])
  }
}
</script>

<style scoped>
.container {
  margin-top: 3rem;
}
</style>