<template> 
        <div class="container">
            <TopNav/>
            <Nuxt />
        </div> 
</template>

<script>
    import TopNav from './partials/TopNav.vue';
    export default {
        components: {
            TopNav
        }
    }
</script>

<style>
    html, body{
        margin: 0;
        height: 100%;
        width: 100%;
    }
    .app-container{
        height: 100%;
        position: relative;
        display: grid;
        grid-template: auto 1fr auto / 1fr;
    }
    .app-content{
        min-height: 100vh;
        padding: 24px;
        display: grid;
        align-items: center;
        justify-items: center;
    }
</style>

 