<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppListCard from './components/AppListCard.vue';
import SelectCard from './components/SelectCard.vue';
import axios from 'axios';

import {store} from './store.js'
export default {
  components:{
    AppHeader,
    AppMain,
    AppListCard,
    SelectCard
  },
  data() {
    return {
      store
    }
  },
  created(){
    this.eseguiListaCarte()
  },
  methods: {
    eseguiListaCarte(){
      let nuovoUrl = `${store.url}${store.selected}`
      
      axios.get(nuovoUrl).then((response) =>{
        store.listaCard = response.data.data
        store.loader = true
      })
    }
  }
}
</script>

<template>
  <AppHeader message="Yu-Gi-Oh API"></AppHeader>
  <SelectCard @selezionaCarta = "eseguiListaCarte"></SelectCard>
  <AppMain  :caricamento ="loader"></AppMain>
</template>

<style lang="scss">
@use '././assets/scss/style.scss' as *;
</style>
