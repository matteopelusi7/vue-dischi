<template>
  <main>

    <div class="container">

      <ul class="card-wrapper">

        <CardMain v-for="(card, i) in cards" :key="i" :cardsItem="card" />

      </ul>

    </div>

  </main>
</template>

<script>

import axios from 'axios'
import CardMain from '../components/CardMain.vue'

export default {

  components: {
    CardMain
  },

  name: 'MainHeader',

  data() {
    return {
      cards: []
    }
  },

  methods: {
    getCards: function() {

      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( res => {
        this.cards = res.data.response
      })

    }
  },

  created() {

    this.getCards()

  }
  
}
</script>

<style scoped lang="scss">

main {

  background-color: #1e2d3b;
  flex-grow: 1;
  display: flex;
  align-items: center;

  .card-wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 30px;
  }

}

</style>
