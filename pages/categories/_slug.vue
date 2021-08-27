<template>
  <div>
    <div>
      <div>
        <h2 class="text-h4 font-weight-bold">ANIMAL</h2>

        <h4 class="text-h6">Some category description goes here</h4>
      </div>

      <v-divider class="my-4"></v-divider>

      <v-row>
        <v-col cols="12" md="6" lg="4" v-for="i in 18" :key="i">
          <v-hover v-slot:default="{ hover }" open-delay="50" close-delay="50">
            <div>
              <v-card
                :color="hover ? 'white' : 'transparent'"
                :elevation="hover ? 12 : 0"
                hover
                to="/detail"
              >
                <v-img
                  src="https://cdn.pixabay.com/photo/2016/11/14/04/45/elephant-1822636_1280.jpg"
                  :aspect-ratio="16 / 9"
                  gradient="to top, rgba(25,32,72,.4), rgba(25,32,72,.0)"
                  height="200px"
                  class="elevation-2"
                  style="border-radius: 16px"
                >
                  <category-button class="pa-4"> ANIMAL </category-button>
                </v-img>

                <v-card-text>
                  <div class="text-h5 font-weight-bold primary--text">
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
  </div>
</template>

<script>
import CategoryButton from "../../components/CategoryButton.vue";
import Signature from "../../components/Signature.vue";
export default {
  components: { Signature, CategoryButton },
};
</script>
