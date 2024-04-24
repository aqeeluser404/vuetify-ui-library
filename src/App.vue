<!-- All vuetify components installed globally -->

<!-- https://vuetifyjs.com/en/features/application-layout/ -->
<!-- https://vuetifyjs.com/en/components/bottom-navigation/#usage -->
<!-- https://vuetifyjs.com/en/components/grids/ -->
<!-- https://vuetifyjs.com/en/styles/css-reset/#bootstrapping -->

<script setup>
  import SideBar from './components/SideBar.vue'
  import ImageGallery from './components/ImageGallery.vue'
</script>

<template>
  <v-app>
    <!-- sidebar layout -->
    <SideBar />
    
    <v-main>
      <!-- grid layout -->
      <ImageGallery />
    </v-main>
    
  </v-app>
</template>
