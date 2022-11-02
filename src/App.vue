<script>
import AppHeader from '@/components/AppHeader.vue';

export default {
  components: {
    AppHeader
   
  },
};
</script>
<template>
  <div id="app container" >
    <AppHeader />
    <div class="">
      <router-view />
    </div>
  </div>
 
</template>
<style>

</style>
