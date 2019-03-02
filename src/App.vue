<template>
  <div class="container">
    <appHeader />
    <hr>
    <div class="row">
      <Servers />
      <appServerDetails />
    </div>
    <hr>
    <appFooter />
  </div>
</template>

<script>
import Header from './components/Shared/Header.vue';
import Footer from './components/Shared/Footer.vue';
import Servers from './components/Server/Servers.vue';
import ServerDetails from './components/Server/ServerDetails.vue';

export default {
  components: {
    appHeader: Header,
    Servers,
    appServerDetails: ServerDetails,
    appFooter: Footer,
  },
};
</script>

<style lang="scss">
</style>
