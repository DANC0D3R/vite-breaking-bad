<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppListCard from './components/AppListCard.vue';
import axios from 'axios';

import {store} from './store.js'
export default {
  components:{
        AppHeader,
        AppMain,
        AppListCard,
      },
      data() {
        return {
          store
        }
      },
      created(){
        this.eseguiListaCarte()
        this.archetypeLista()
      },
      methods: {
        eseguiListaCarte(){
          axios.get(store.url).then((response) =>{
            store.listaCard = response.data.data.slice(0,20)
            store.loader = true
          })
        },
        archetypeLista(){
          axios.get(store.archetype).then((response) =>{
            store.archetypeArray = response.data
          })
        }
      },
    }
</script>

<template>
  <AppHeader message="Yu-Gi-Oh API"></AppHeader>
  <SelectCard></SelectCard>
  <AppMain :caricamento ="loader"></AppMain>
</template>

<style lang="scss">
@use '././assets/scss/style.scss' as *;
</style>
