<template>
  <v-app>
    <!-- Navigation Bar -->
    <v-navigation-drawer height="100%" permanent absolute expand-on-hover app>
      <!-- Navigation Bar -->
      <!-- Profile Header -->
      <v-list>
        <v-list-item link class="px-2">
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/men/11.jpg"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="font-weight-bold">PLAZA, ORLY O.</v-list-item-title>
            <v-list-item-subtitle>orly.plaza@hcdc.edu.ph</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <!-- Lower List-item-icons -->
      <!-- My Files -->
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-folder</v-icon>
        </v-list-item-icon>
        <v-list-item-title>My Files</v-list-item-title>
      </v-list-item>

      <!-- Flutter  -->
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-android-studio</v-icon>
        </v-list-item-icon>
        <v-list-item-title>Flutter Codes</v-list-item-title>
      </v-list-item>

      <!-- Python -->
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-language-python</v-icon>
        </v-list-item-icon>
        <v-list-item-title>Python Codes</v-list-item-title>
      </v-list-item>

      <!-- JavaScript -->
      <v-list-item link>
        <v-list-item-icon>
          <v-icon>mdi-language-javascript</v-icon>
        </v-list-item-icon>
        <v-list-item-title>JavaScript Codes</v-list-item-title>
      </v-list-item>

    </v-navigation-drawer>
    <!-- Sizes your content based upon application components -->

    <!-- Header Column -->
    <v-main>

      <!-- Provides the application the proper gutter -->
      <v-container fluid>

        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <!-- Router -->
    <v-footer class="" app dark padless>
      <!-- -->
      <v-card class="text-center" flat tile width="100%">

        <!-- Card for Icons -->
        <v-card-text>
          <v-btn class="mx-3" icon v-for="icon in icons" :key="icon">
            <v-icon dense>{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
        <v-divider></v-divider>

        <!-- Additional Info -->
        <!-- <v-row class="mx-4"> -->
        <!-- Column 1 -->
        <!-- <v-col>
            <v-card flat>
              <v-card-text>plazaorl.2000@gmail.com</v-card-text>
              <v-spacer></v-spacer>
            </v-card>
          </v-col> -->

        <!-- Column 2 -->
        <!-- <v-col>
            <v-card flat>
              <v-card-text>P4A Sabang Lingig Surigao del sur, PH 8312</v-card-text>
            </v-card>
          </v-col> -->

        <!-- Column 3 -->
        <!-- <v-col>
            <v-card flat>
              <v-card-text>P4A Sabang Lingig Surigao del sur, PH 8312</v-card-text>
            </v-card>
          </v-col>
        </v-row> -->

        <!-- Card for Text -->
        <v-card-text>
          <strong>&copy;2022 | {{ Author }}</strong>
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
      Author: 'ENGR. PLAZA ORLY',
    }
  }
}
</script>
