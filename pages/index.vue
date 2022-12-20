<template>
  <v-app>
    <v-main>
      <!-- Header -->
      <v-card class="text-center mt-5 mb-5" flat tile width="100%">
        <!-- Card for Icons -->
        <v-row>
          <v-card-text link>
            <v-btn plain>
              <v-img src="logo/or1.png" max-width="55" max-height="55"></v-img>
            </v-btn>
            <v-btn class="mx-6" v-for="nav_text in header_navigation_text" :key="nav_text" plain link>
              {{ nav_text }}
            </v-btn>
          </v-card-text>
        </v-row>
      </v-card>

      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- Greetings -->
        <v-card class="text-center" flat tile width="100%">
          <v-card-text>
            <div class="text-h2 font-weight-black">
              ORLY PLAZA
              <div class="text-h6 font-weight-black">
                IoT Specialist
              </div>
            </div>
          </v-card-text>
        </v-card>

        <!-- Profile Image -->
        <v-card class="text-center mx-auto pa-3" flat tile>
          <v-row justify="center">
            <v-img class="rounded-circle" max-width="150" max-height="150" src="Images/pixelface.png">
            </v-img>
          </v-row>
        </v-card>

        <!-- Introduction Text -->
        <v-card class="text-left mx-auto pa-3" max-width="50%" flat tile>
          <v-row>
            <v-col>
              <p class="text-center mt-10 mb-10">
                {{ Introduction_text }}
              </p>
            </v-col>
          </v-row>
        </v-card>

        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <!-- Router -->
    <v-footer class="" app padless>
      <v-card class="text-center" flat tile width="100%">

        <!-- Card for Icons -->
        <v-card-text>
          <v-btn class="mx-3" icon v-for="icon in icons" :key="icon">
            <v-icon dense>{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
        <!-- Card for Text -->
        <v-card-text>
          <p>{{ Author }} | &copy;2022</p>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script lang="ts">

export default {
  name: 'index',
  data: () => {
    return {
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-instagram',
        'mdi-github',
        'mdi-linkedin',
      ],

      header_navigation_text: [
        'Home',
        'About',
        'Contact',
      ],

      Author: 'ENGR. PLAZA ORLY',
      Introduction_text: "I am a self-motivated Computer Engineer and an aspiring Python developer, and I use C++ for research and development. I'm fascinated by technology innovation. to get an opportunity that allows me to showcase my skills and contribute to the company's growth.",
    }
  }
}
</script>
