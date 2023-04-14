<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppLinks from './components/AppLinks.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppLinks,
    AppFooter
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppLinks />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>