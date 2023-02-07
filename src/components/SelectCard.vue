<script>
import {store} from '../store'
    export default {
            data(){
                return{
                    store
                }
            }
    }
</script>
<template lang="">
    <div>
        <div class="container" style="padding-left: 0;">
            <div class="row">
                <div class="col-3 select-race">
                    <select  class="form-select mt-2 " aria-label="Default select example" v-model="selectOption">
                        <option disable-value="">Scegli La razza</option>
                        <option v-for="(item, index) in store.archetypeArray" :key="index">{{item.archetype_name}}</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    
</style>