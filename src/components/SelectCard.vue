<script>
import {store} from '../store'
import axios from 'axios'
    export default {
        data(){
            return{
                store,
                arrayArchetype:[]
            }
        },
        created(){
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((response) =>{
                this.arrayArchetype = response.data
            })
        }
    }
</script>

<template lang="">
    <div>
        <div class="container" style="padding-left: 0;">
            <div class="row">
                <div class="col-3 select-race">
                    <select class="form-select mt-2" aria-label="Default select example" v-model="store.selected" @change="$emit('selezionaCarta')">
                        <option value="" disable-value>Seleziona Archetyipo</option>
                        <option v-for="item in arrayArchetype" :value="item.archetype_name">{{item.archetype_name}}</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
</template>

<!-- Stile -->
<style lang="scss">
    
</style>