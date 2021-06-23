<template>
  <v-row fluid justify="center" align="center">
    <v-col cols="12" sm="8" md="9">
      <!-- <div class="text-center">
        <logo />
        <vuetify-logo />
      </div> -->
      <v-spacer />

      <section>
        <v-row>
          <v-col>
            <h3 class="text-center">
              About Me
            </h3>
          </v-col>
        </v-row>

        <v-row>
          <v-col sm="2">
            Icons
          </v-col>
          <v-col sm="10">
            <p>
              Entrepreneurial self-starter in the process of learning Node and Angular. Currently seeking a Front-end Web Developer position where I can use my strengths in HTML, CSS, SCSS and JS to create modern web pages and intuitive UI. My biggest passions building for the web are combining design with the world of development, creating DRY and reusable code and learning about new updates and technology to better my workflow and knowledge. I am also a creative individual who enjoys working with Adobe Creative Suite and various audio and sound design software.
            </p>
          </v-col>
        </v-row>
      </section>

      <section>
        <v-row>
          <v-col>
            <h3 class="text-center">
              My Recent Work
            </h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <v-sheet
              class="mx-auto"
              elevation="8"
            >
              <v-slide-group
                v-model="model"
                class="pa-4"
                show-arrows
                center-active
              >
                <v-slide-item
                  v-for="n in 15"
                  :key="n"
                  v-slot="{ active, toggle }"
                >
                  <v-card
                    :color="active ? 'primary' : 'grey lighten-1'"
                    class="ma-4"
                    height="200"
                    width="300"
                    @click="toggle"
                  >
                    <v-row
                      class="fill-height"
                      align="center"
                      justify="center"
                    >
                      <v-scale-transition>
                        <v-icon
                          v-if="active"
                          color="white"
                          size="48"
                          v-text="'mdi-close-circle-outline'"
                        />
                      </v-scale-transition>
                    </v-row>
                  </v-card>
                </v-slide-item>
              </v-slide-group>

              <v-expand-transition>
                <v-sheet
                  v-if="model != null"
                  height="200"
                  tile
                >
                  <v-row
                    class="fill-height"
                    align="center"
                    justify="center"
                  >
                    <h3 class="text-h6">
                      Selected {{ model }}
                    </h3>
                  </v-row>
                </v-sheet>
              </v-expand-transition>
            </v-sheet>
          </v-col>
        </v-row>
      </section>

      <section>
        <v-row>
          <v-col>
            <h3 class="text-center">
              Skills and Technologies
            </h3>
          </v-col>
        </v-row>
      </section>

      <section>
        <v-row>
          <v-col>
            <h3 class="text-center">
              Professional Experience
            </h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col />
          <v-col />
        </v-row>
      </section>
    </v-col>
  </v-row>
  </section>
  </v-col>
  </v-row>
</template>

<script>
// import Logo from '~/components/Logo.vue'
// import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  // components: {
  //   Logo,
  //   VuetifyLogo
  // }
  data: () => ({
    model: null
  })
}
</script>
