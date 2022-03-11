<template>
  <main>

    <div class="container">

      <OptionBar @search="selectGenre"/>

      <ul class="card-wrapper" v-if="cards.length == 10">

        <CardMain v-for="(card, i) in filterCard" :key="i" :cardsItem="card" />

      </ul>

      <div v-else>

        <LoaderContent />

      </div>

    </div>

  </main>
</template>

<script>

import axios from 'axios'
import CardMain from '../components/CardMain.vue'
import LoaderContent from '../components/Loader.vue'
import OptionBar from './Option.vue'

export default {

  components: {
    CardMain,
    LoaderContent,
    OptionBar
  },

  name: 'MainHeader',

  data() {
    return {
      cards: [],
      searchBar: '',
    }
  },

  computed: {

    filterCard() {

      if (this.searchBar === 'All') {
        return this.cards
      }
        return this.cards.filter( (item) => {
        return item.genre.includes(this.searchBar)
      })

    },

  },

  methods: {

    getCards: function() {
      
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( res => {
        this.cards = res.data.response
      })

    },

    selectGenre(search) {
      this.searchBar = search
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
