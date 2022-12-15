<template>
  <!-- App.vue -->
  <v-app>
    <v-navigation-drawer permanent expand-on-hover app>
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

    <!-- <v-app-bar app> -->
    <!-- -->
    <!-- </v-app-bar> -->

    <!-- Sizes your content based upon application components -->
    <v-main>

      <!-- Provides the application the proper gutter -->
      <v-container fluid>

        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer dark padless app>
      <!-- Footer -->
      <v-card class="flex" flat tile>
        <v-card-title class="teal">
          <!-- Icon As Button -->
          <v-spacer></v-spacer>

          <!-- facebook -->
          <v-btn class="mx-4" dark icon link>
            <v-icon size="24px">mdi-facebook</v-icon>
          </v-btn>

          <!-- twitter -->
          <v-btn class="mx-4" dark icon link>
            <v-icon size="24px">mdi-twitter</v-icon>
          </v-btn>

          <!-- github -->
          <v-btn class="mx-4" dark icon link>
            <v-icon size="24px">mdi-github</v-icon>
          </v-btn>

          <!-- linkedin -->
          <v-btn class="mx-4" dark icon link>
            <v-icon size="24px">mdi-linkedin</v-icon>
          </v-btn>

        </v-card-title>
      </v-card>

    </v-footer>
  </v-app>
</template>

<script lang="ts">
export default {
  name: 'index',
  data() {
    return {
      x: 20,
    }
  }
}
</script>