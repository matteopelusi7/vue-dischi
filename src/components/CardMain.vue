<template>

  <li class="card-item">

    <div class="img-container">
      <figure class="img-wrapper">
        <img :src="cardsItem.poster" alt="">
      </figure>
    </div>

    <div class="card-info">
      <h3 class="title-card">{{ cardsItem.title }}</h3>
      <p class="subtitle-card">{{ cardsItem.author }}</p>
    </div>

  </li>

</template>

<script>
export default {
  name: 'CardMain',

  props: {
    cardsItem: {
      type: Object,
      require: true
    }
  }
  
}
</script>

<style scoped lang="scss">

.card-item {

  width: calc( (100% / 5) - 30px);
  height: 300px;
  background-color: #2e3a46;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 15px;
  padding: 20px;

  .img-container {
    height: 150px;
  }

  .card-info {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
  }

  .title-card {
    color: white;
    text-transform: uppercase;
    text-align: center;
  }

  .subtitle-card {
    color: grey;
    text-align: center;
  }

  .img-wrapper {
    width: 100%;
    aspect-ratio: 1/1;
  }

}

</style>
