<template>
  <VModal type="error" title="Archive your profile?" msg="Are you sure you want to archive your profile? You will be able to restore it."/>
  <VModal type="info" title="Your request will be reviewed" msg="Site administrator will review your data and respond to a request"/>
  <VModal type="warning" title="Your request will be reviewed" msg="Site administrator will review your data and respond to a request"/>
  <VModal type="success" title="Your request will be reviewed" msg="Site administrator will review your data and respond to a request"/>
</template>

<script>
import VModal from './components/VModal.vue'

export default {
  name: 'App',
  components: {
    VModal
  }
}
</script>

<style>
#app {
  font-family: 'Poppins', sans-serif;
}
</style>
