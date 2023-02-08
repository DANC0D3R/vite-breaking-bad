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
            <div class="container row">
                <div class="col-12 p-0 pt-3 pb-3 d-flex align-items-center">
                    <img src="../assets/img/yu-gi-oh-logo.png" alt="logo">
                    <h1>{{message}}</h1>
                </div>
            </div>
        </div>
    </header>
</template>

<!-- Stile -->
<style lang="scss">
    header{
        background-color: #FFFFFF;
        .container{
            margin: 0 auto;
            padding: 0;
            img{
            width: 10rem;
        }
        h1{
            color: #000000;
        }
        }
    }
</style>