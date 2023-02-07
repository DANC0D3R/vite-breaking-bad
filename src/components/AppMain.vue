<script>
import AppListCard from './AppListCard.vue';
import SelectCard from './SelectCard.vue';
import {store} from '../store'
    export default {
        components:{
            AppListCard,
            SelectCard,
        },
        data(){
            return{
                store
            }
        }
    }
</script>
<template>
    <div>
        <div class="container bg-white mt-2">
            <div class="row">
                <div >
                    <SelectCard :tipo="store.listaCard"></SelectCard>
                    <!-- Caricamento -->
                    <div v-if="store.loader == false" class="col-12 m-5 d-flex justify-content-center">
                        <div class="spinner-border" role="status"></div>
                    </div>
                    <!-- Card -->
                    <div v-else class="col-12  my-2 d-flex flex-wrap justify-content-between">
                        <AppListCard v-for="(item, index) in store.listaCard" :key="index" :carta="item"></AppListCard>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    
</style>