<!-- All vuetify components installed globally -->
<!-- https://vuetifyjs.com/en/features/application-layout/  24:36 -->

<script setup>
  import SideBar from './components/SideBar.vue'
  import ImageGallery from './components/ImageGallery.vue'
</script>

<template>
  <v-app>
    <!-- SIDEBAR -->
    <SideBar />
    <v-main>
      <ImageGallery />

    </v-main>
  </v-app>
</template>
