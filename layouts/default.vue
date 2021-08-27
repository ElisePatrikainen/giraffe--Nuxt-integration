<template>
  <v-app>
    <the-navigation-bar></the-navigation-bar>
    <v-main class="pl-12 pr-12">
      <v-container fluid>
        <v-row>
          <v-col cols="12" lg="8">
            <Nuxt />
          </v-col>
          <v-col>
            <div>
              <the-sidebar />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <the-footer></the-footer>
  </v-app>
</template>

<script>
import TheFooter from "./components/TheFooter.vue";
import TheNavigationBar from "./components/TheNavigationBar.vue";
import TheSidebar from "./components/TheSidebar.vue";

export default {
  components: {
    TheNavigationBar,
    TheFooter,
    TheSidebar,
  },
};
</script>
