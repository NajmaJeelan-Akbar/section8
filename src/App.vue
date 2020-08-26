<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <app-user></app-user>
            </div>
        </div>
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue';

    export default {
      
        components: {
            appUser: HelloWorld
        }
    }
</script>

<style>
    div.component {
        border: 1px solid black;
        padding: 30px;
    }
</style>
