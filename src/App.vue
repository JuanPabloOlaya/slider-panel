<template>
  <div id="app">
    <div class="container">
      <nav-app />
      <div class="content">
        <header-app />
        <div class="main"></div>
      </div>
    </div>
  </div>
</template>

<script>
import NavApp from '@/components/common/NavApp.vue';
import HeaderApp from '@/components/common/HeaderApp.vue';

export default {
  name: 'App',
  components: {
    NavApp,
    HeaderApp,
  },
};
</script>
<style lang="scss" src="@/assets/scss/main.scss"></style>
