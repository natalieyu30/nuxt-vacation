<template>
  <div>
    <b-button id="show-btn" @click="showModal">Reserve a Place</b-button>

    <b-modal ref="my-modal" hide-footer title="When are you planning to go?" class="reserve-modal">
      <div class="d-flex">
        <div class="text-container mr-2">
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur blanditiis ex ab eligendi rerum deleniti mollitia vitae? Placeat accusamus architecto deserunt rem ab! Autem iusto suscipit porro enim a! Perferendis.</p>
        </div>
        <vc-date-picker
          :value="null"
          color="green"
          is-range
        />
      </div>
      <b-button 
        variant="outline-danger"
        @click="() => {
          addItem(product.id)
          hideModal()
        }"
      >Reserve</b-button>
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
  export default {
    props: ['product'],
    methods: {
      showModal() {
        this.$refs['my-modal'].show()
      },
      hideModal() {
        this.$refs['my-modal'].hide()
      },
      toggleModal() {
        // We pass the ID of the button that we want to return focus to
        // when the modal has hidden
        this.$refs['my-modal'].toggle('#toggle-btn')
      },
      ...mapMutations(['addItem'])
    }
  }
</script>

<style scoped>
button {
  /* width: 100%; */
  border: none;
  color: white;
  font-weight: 700;
  margin-top: 1rem;
  padding: 0.8rem 3rem;
  border-radius: 100rem;
  background-color: green;
  color: white;
  font-weight: 700;
  transition: 0.5s;
}
button:hover {
  background-color: rgb(7, 148, 7);
}
p {
  color: grey
}
.text-container {
  padding: 0.5rem
}

</style>