<script>
import AppListCard from './AppListCard.vue';
import {store} from '../store'
    export default {
        components:{
            AppListCard,
        },
        data(){
            return{
                store
            }
        },
    }
</script>

<template>
    <div>
        <div class="container bg-white mt-2">
            <div class="row">
                <div >
                    <!-- Caricamento -->
                    <div v-if="store.loader == false" class="col-12 m-5 d-flex flex-column justify-content-center align-items-center">
                        <div class="spinner-border" role="status"></div>
                        <h3 class="pt-5" >Scegli l'archetipo per visualizzare le carte</h3></div>
                    <!-- Cards -->
                    <div v-else class="col-12 my-2 d-flex flex-wrap justify-content-between">
                        <AppListCard v-for="(item, index) in store.listaCard" :key="index" :carta="item"></AppListCard>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<!-- Stile -->
<style lang="scss">

</style>