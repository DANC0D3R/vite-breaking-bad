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

      },
      methods: {
        eseguiListaCarte(){
          axios.get(store.url).then((response) =>{
            store.listaCard = response.data.data.slice(0,20)
          })
        }
      },
      
    }
</script>

<template>
  <AppHeader message="Yu-Gi-Oh API"></AppHeader>
  <AppMain></AppMain>
</template>

<style lang="scss">
@use '././assets/scss/style.scss' as *;
</style>
