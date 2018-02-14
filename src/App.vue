<template>
  <router-view></router-view>
</template>

<script>
export default {
  name: 'app',
  created () {
    this.$store.dispatch('LOAD_SERVER_DETAILS').then(response => {
      console.log('Got some data, now lets show something in this component')
    }, error => {
      console.error('Got nothing from server. Prompt user to check internet connection and try again')
    })
  }
}
</script>

<style>
  /* Import Font Awesome Icons Set */
  @import '~flag-icon-css/css/flag-icon.min.css';
  /* Import Font Awesome Icons Set */
  $fa-font-path: '~font-awesome/fonts/';
  @import '~font-awesome/css/font-awesome.min.css';
  /* Import Simple Line Icons Set */
  $simple-line-font-path: '~simple-line-icons/fonts/';
  @import '~simple-line-icons/css/simple-line-icons.css';
  /* Import Bootstrap Vue Styles */
  @import '~bootstrap-vue/dist/bootstrap-vue.css';
</style>
<style lang="scss">
  // Import Main styles for this application
  @import './scss/style';
</style>
