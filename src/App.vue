<template>
  <v-app>
    <v-content>
      <Header/>
      <Server/>
      <Footer/>
    </v-content>
  </v-app>
</template>

<script>
import Server from './components/Server';
import Footer from './components/Footer'
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    Server,
    Header,
    Footer
  },
  data: () => ({
    //
  }),
};
</script>

<style scoped>
  #app {
    background-color: #323131;
    padding: 2%;
  }
  .container {
    margin-bottom: 6%;
  }

</style>
