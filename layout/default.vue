<template>
    <div class="app-container">

        <TopNav/>

         

        <div class="app-content">
            <nuxt />
        </div>

        

    </div>
</template>

<script>
    import TopNav from './partials/TopNav.vue';
    export default {
        components: {
            TopNav
        },
        computed: {
            isSidebar() {
                return this.$store.getters['nav/toggleSidebar']
            }
        },
        watch: {
            '$route': function() {
                if (process.client && this.isSidebar && window.innerWidth < 768) {
                    this.$store.dispatch('nav/toggleSidebar')
                }
            },
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

 