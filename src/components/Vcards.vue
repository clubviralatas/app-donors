<template>
  <div class="row">
    <q-card inline>
      <q-item>
        <q-item-side avatar="statics/fotoNelci.jpg"/>
        <q-item-main>
          <q-item-tile label>Nelci Gomes</q-item-tile>
          <!--<q-item-tile sublabel>Voluntária ABPA</q-item-tile>-->
        </q-item-main>
       <q-chip icon="pets" color="yellow-9">
          VIP
        </q-chip>
      </q-item>
      <q-card-media>
        <img src="~assets/fotoMiloca.jpg">
      </q-card-media>
      <div class="background-club-viralatas">
          <q-card-title slot="overlay">
            <img src="statics/dog.svg" height="32" alt="Dog">
            <span class="light relative-position" color="">
            Mila Cachorrinha Linda
          </span>
            <span slot="subtitle">Vonlutária ABPA</span>
          </q-card-title>
          <q-card-main slot="overlay">
            Nivel de Doador:
            <q-rating v-model="ratingModel" :max="5"></q-rating>
          </q-card-main>
          <q-card-actions slot="overlay">
            <q-btn icon="fa-facebook-square" color="primary">Compartilhar</q-btn>
            <q-btn icon="fa-instagram" color="red">Compartilhar</q-btn>
          </q-card-actions>
      </div>
    </q-card>
  </div>
</template>

<script>
  import {
    QBtn,
    QChip,
    QRating,
    QCardMedia,
    QCardTitle,
    QCard,
    QCardMain,
    QItem,
    QItemMain,
    QItemTile,
    QItemSide,
    QCardActions
  } from 'quasar'

  export default {
    components: {
      QBtn,
      QChip,
      QRating,
      QCardMedia,
      QCardTitle,
      QCard,
      QCardMain,
      QItem,
      QItemMain,
      QItemTile,
      QItemSide,
      QCardActions
    },
    data () {
      return {
        name: 'Nelci Gomes',
        memberSince: new Date('2017-07-01'),
        ratingModel: 4
      }
    },
    methods: {}
  }
</script>

<style lang="stylus">
  .background-club-viralatas
    background-image url(/statics/clubVL-40.png)
    background-size 115px
    background-repeat no-repeat
    background-position right top
    margin-right 5px
    margin-top 5px

</style>
