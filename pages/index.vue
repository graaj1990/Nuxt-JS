<template>
<div class="container">
  Home Page
  <nuxt/>
</div>

  
</template> 

<script lang="ts">
import Vue from 'vue'
import TopNav from '~/layout/partials/TopNav.vue'

export default Vue.extend({
  components: { TopNav },
  name: 'IndexPage'
})
</script>
