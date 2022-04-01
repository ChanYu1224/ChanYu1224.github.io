<template>
  <v-app>
    <NavigationBar/>
    <v-main>
      <IntroductionPane id="introduction"/>
      <WorksPane id="works"/>
      <ContactPane id="contact"/>
    </v-main>
  </v-app>
</template>

<script>
import NavigationBar from './components/NavigationBar.vue'
import IntroductionPane from './components/IntroductionPane.vue'
import WorksPane from './components/WorksPane.vue'
import ContactPane from './components/ContactPane.vue'

export default {
  name: 'App',
  components: {
    NavigationBar,
    IntroductionPane,
    WorksPane,
    ContactPane,
  },
};
</script>
