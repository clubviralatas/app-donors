<template>
  <!-- Don't drop "q-app" class -->
  <div id="q-app">
    <q-layout
      ref="layout"
      view="lHh Lpr fff"
      :left-class="{'bg-red-1': true}"
      :header-class="{'bg-red-4': true}"
      :class="{'bg-red-1': true}"
    >
      <q-toolbar slot="header" class="glossy bg-red-4">
        <q-btn
          flat
          @click="$refs.layout.toggleLeft()"
        >
          <q-icon name="menu"/>
        </q-btn>

        <q-toolbar-title>
          Club ViraLatas
          <div slot="subtitle">Sustentabilidade para ONGs</div>
        </q-toolbar-title>
      </q-toolbar>

      <div slot="left">
        <!--
          Use <q-side-link> component
          instead of <q-item> for
          internal vue-router navigation
        -->

        <q-list no-border link inset-delimiter>
          <!--<q-list-header>Opções da Aplicação</q-list-header>-->
          <q-side-link item to="/">
            <q-item-side icon="home"/>
            <q-item-main label="Home" sublabel="Tela de Boas Vindas"/>
          </q-side-link>
          <q-side-link item to="/vcards">
            <q-item-side icon="card membership"/>
            <q-item-main label="Cartão de Membro" sublabel="Detalhes cartão fidelidade"/>
          </q-side-link>
        </q-list>
      </div>
      <router-view/>
    </q-layout>
  </div>
</template>

<script>
  import {
    QLayout,
    QToolbar,
    QToolbarTitle,
    QBtn,
    QIcon,
    QList,
    QListHeader,
    QItem,
    QItemSide,
    QItemMain,
    QSideLink
  } from 'quasar'
  /*
   * Root component
   */
  export default {
    components: {
      QLayout,
      QToolbar,
      QToolbarTitle,
      QBtn,
      QIcon,
      QList,
      QListHeader,
      QItem,
      QItemSide,
      QItemMain,
      QSideLink
    }
  }
</script>

<style></style>
