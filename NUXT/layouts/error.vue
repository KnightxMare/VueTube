<template>
  <v-app>
    <center>

      <v-icon size="100">mdi-alert-circle</v-icon>
      <h1 class="grey--text">An error occured!</h1>
      <v-btn to="/">Reload Application</v-btn>
      <v-btn to="/logs">Show Logs</v-btn>


      <div style="margin-top: 5em; color: #999; font-size: 0.75em;">
        <div style="font-size: 1.4em;">Error Information</div>
        <div>Code: {{ error.statusCode }}</div>
        <div>Path: {{ this.$route.fullPath }}</div>
      </div>

    </center>
  </v-app>
</template>

<script>
export default {
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null
    }
  }
}
</script>
