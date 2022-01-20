<template>
  <div id="app">
    <EventsAdvisor/>
    <Header/>
    <Main/>
    <Footer/>



  </div>
</template>

<script>
import EventsAdvisor from "./components/EventsAdvisor.vue";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    EventsAdvisor,
    Header,
    Main,
    Footer,
  },
};
</script>

<style lang="scss">
@import './style/variables.scss';
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100;200;300;400;500;600;700;800;900&family=The+Nautigal:wght@400;700&display=swap');
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import './style/general.scss';

#app {
  overflow: hidden;
}

</style>
