<template>
<div class="Hero container">
  <div class="text-container">
    <h1 class="header">Find your Vacation Experience</h1>
    <p class="snippet">Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur culpa eos illum doloremque nobis nihil aspernatur dolores quis ratione earum?</p>
    <button class="button btn">Start Looking</button>
  </div>
  <img src="~assets/img/navigator.png" alt="" class="image">
</div>

  
</template>

<script>
export default {

}
</script>

<style scoped>
.Hero {
  height: 50vh;
  position: relative;
  display: flex;
  padding: 5rem 0;
  align-items: flex-start;
  justify-content: space-between;
}
.text-container {
  display: block;
  width: 50%;
}
.header {
  font-weight: 900;
  font-size: 3.5rem;
}
.snippet {
  color: grey;
  font-size: 1.1rem;
}
.image {
  width: 27.5rem;
  margin-top: 2rem;
  overflow: hidden;
}
.overlay {
  background: rgba(0, 0, 0, 0);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
.button {
  display: block;
  padding: 0.9rem 3.5rem;
  border-radius: 100rem;
  background-color: #17a714;
  color: white;
  width: 20rem;
  font-weight: 700;
  transition: 0.5s;
}
.button:hover {
  width: 21.5rem;
}
@media (max-width: 750px) {
  .Hero {
    height: 40vh;
    display: block;
    padding: 2rem 0;
    margin: 0 auto;
  }
  .text-container {
    width: 90%;
    margin-top: 0;
  }
  .image {
    display: none;
  }
}

@media (max-width: 420px) {
  .Hero {
    margin-bottom: 8rem;
  }
  .header {
    font-weight: 700;
    font-size: 2.4rem;
  }
  .snippet {
    font-size: 0.9rem;
  }
  .button {
    display: block;
    padding: 0.8rem 3rem;
    width: 16rem;
  }
  .button:hover {
    width: 16.5rem;
  }
}
</style>