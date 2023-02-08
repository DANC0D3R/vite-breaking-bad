<script>
    export default {
        name: 'AppListCard',
        props:{
            carta: Object
        }
    }
</script>

<template>
    <div>
        <div>
            <div class="card p-2 my-2" style="width: 19rem; height: 34rem; background-color: #D48F38;">
                <img :src="carta.card_images[0].image_url" class="card-img-top" alt="url-immagine">
                <div class="card-body">
                    <h5 class="card-title">{{carta.name}}</h5>
                    <h6>{{carta.archetype}}</h6>
                </div>
            </div>
        </div>
    </div>
</template>

<!-- Stile -->
<style lang="scss">

</style>