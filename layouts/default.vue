<template>
  <v-app>
    <the-navigation-bar></the-navigation-bar>
    <v-main>
      <v-container>
        <div>
          <v-row>
            <v-col cols="12" lg="12" xl="8">
              <Nuxt />
            </v-col>
            <v-col>
              <the-sidebar />
            </v-col>
          </v-row>
        </div>
      </v-container>
    </v-main>
    <the-footer></the-footer>
  </v-app>
</template>

<script>
import TheFooter from './components/TheFooter.vue'
import TheNavigationBar from './components/TheNavigationBar.vue'
import TheSidebar from './components/TheSidebar.vue'

export default {
  components: {
    TheNavigationBar,
    TheFooter,
    TheSidebar,
  },
}
</script>
