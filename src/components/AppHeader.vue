<script>
        export default {
            props:{
                message: String
            }
        }
</script>
<template>
    <header>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 p-3 border border-light text-light d-flex align-items-center">
                    <img src="../assets/img/yu-gi-oh-logo.png" alt="logo">
                    <h1 class="ms-3">{{message}}</h1>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
    header{
        background-color: #FFFFFF;
        img{
            width: 6rem;
            height: 2rem;
        }
        h1{
            color: #000000;
        }
    }
</style>