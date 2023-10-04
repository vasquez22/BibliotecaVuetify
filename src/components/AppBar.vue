<template>
  <!-- Este commponente mostrar una barra de aplicacion -->
  <v-app-bar scroll-behavior="hide" color="teal-darken-4">
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-app-bar-title>Vuetify</v-app-bar-title>
    
    <!-- agregar un boton para navegar a la ruta -->
    <v-btn icon="mdi-home" to="/"></v-btn>
  </v-app-bar>
</template>


<script>
export default {
  name: "AppBar",
};
</script>