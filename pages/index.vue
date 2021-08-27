<template>
  <div>
    <div class="pt-16">
      <h2 class="text-h4 font-weight-bold pb-4">Recommended For You</h2>

      <v-row>
        <v-col v-for="i in 6" :key="i" cols="12" md="6" lg="4">
          <v-hover v-slot="{ hover }" open-delay="50" close-delay="50">
            <div>
              <v-card
                flat
                :color="hover ? 'white' : 'transparent'"
                :elevation="hover ? 12 : 0"
                hover
                to="/detail"
              >
                <v-img
                  src="https://cdn.pixabay.com/photo/2020/12/23/14/41/forest-5855196_1280.jpg"
                  :aspect-ratio="16 / 9"
                  gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
                  height="200px"
                  class="elevation-2"
                  style="border-radius: 16px"
                >
                  <category-button class="pa-4"> TIPS </category-button>
                </v-img>

                <v-card-text>
                  <div class="text-h5 font-weight-bold" style="color: black">
                    How to write an awesome blog post in 5 steps
                  </div>

                  <div class="text-body-1 py-4">
                    Ultrices sagittis orci a scelerisque. Massa placerat duis
                    ultricies lacus sed turpis
                  </div>
                  <signature />
                </v-card-text>
              </v-card>
            </div>
          </v-hover>
        </v-col>
      </v-row>
    </div>

    <div class="pt-16">
      <h2 class="text-h4 font-weight-bold pb-4">Featured</h2>

      <v-row>
        <v-col v-for="i in 3" :key="i" cols="6" lg="4">
          <v-card flat dark>
            <v-img
              src="https://cdn.pixabay.com/photo/2019/10/29/14/46/landscape-4587079_1280.jpg"
              :aspect-ratio="16 / 9"
              gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
              height="400px"
              class="elevation-2 fill-height"
            >
              <div class="d-flex flex-column justify-space-between fill-height">
                <category-button style="padding: 16px">ANIMALS</category-button>
                <v-card-text>
                  <div
                    class="text-h5 py-3 font-weight-bold"
                    style="line-height: 1.2"
                  >
                    15 things I have always wondered about birds
                  </div>
                  <signature />
                </v-card-text>
              </div>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </div>

    <div class="pt-16">
      <h2 class="text-h4 font-weight-bold">Latest Posts</h2>

      <div>
        <v-row v-for="i in 6" :key="i" class="py-4">
          <v-col cols="12" md="4">
            <v-card flat height="100%">
              <v-img
                src="https://cdn.pixabay.com/photo/2021/01/27/06/54/nova-scotia-duck-tolling-retriever-5953883_1280.jpg"
                :aspect-ratio="16 / 9"
                height="100%"
              ></v-img>
            </v-card>
          </v-col>

          <v-col>
            <div>
              <category-button>TRAVEL</category-button>
              <h3 class="text-h4 font-weight-bold pt-3">
                Ut enim blandit volutpat maecenas volutpat blandit
              </h3>
              <p class="text-h6 font-weight-regular pt-3 text--secondary">
                Duis aute irure dolor in reprehenderit in voluptate velit esse
                cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
                cupidatat non proident, sunt in culpa qui officia deserunt
                mollit anim id est laborum.
              </p>
              <signature />
            </div>
          </v-col>
        </v-row>
      </div>
    </div>
  </div>
</template>

<script>
import CategoryButton from "../components/CategoryButton.vue";
import Signature from "../components/Signature.vue";

export default {
  components: { CategoryButton, Signature },
  layout: "home",
};
</script>
