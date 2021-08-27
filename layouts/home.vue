<template>
  <v-app >
    <the-navigation-bar></the-navigation-bar>
    <v-main class="pl-12 pr-12">      
      <v-container fluid>
        <div>
          <v-card to="detail">
            <v-img
              src="https://images.pexels.com/photos/3244513/pexels-photo-3244513.jpeg"
              gradient="to top, rgba(25,32,72,.7), rgba(25,32,72,.0)"
              :aspect-ratio="16 / 9"
              height="500px"
              dark
            >
              <div style="height: 100%; position: relative">
                <div style="position: absolute; bottom: 0; left: 0; padding: 16px;">
                      <v-btn color="blue darken-1" dark>Travel</v-btn>
                      <h2 class="text-h3 py-3" style="line-height: 1.2">
                        Great Travel Blogs From Around The World To Inspire You
                      </h2>
                      <div style="display: flex">
                      <v-avatar class="elevation-4" color="blue darken-1">
                        <v-icon>mdi-feather</v-icon>
                      </v-avatar>
                      <div class="text-h6 pl-2">Yan Lee · 22 July 2019</div>
                      </div>
                </div>
              </div>
            </v-img>
          </v-card>
          <v-row>
            <v-col cols="12" lg="8">
              <Nuxt />
            </v-col>
            <v-col>
              <div class="pt-16">
                <the-sidebar />
              </div>
            </v-col>
          </v-row>
        </div>
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
