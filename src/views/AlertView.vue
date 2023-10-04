<template>
    <v-container :fluid="true">
        <h1 class="text-green-darken-4">Alerta</h1>
        <v-btn prepend-icon="mdi-bell-ring" color="indigo" rounded="xl" @click="alertState = true">Mostrar Alerta</v-btn>
        <br><br>
        <!-- alerta -->
        <v-alert closable v-model="alertState" icon="mdi-information" title="Restuesta" text="El producto ha sido guardado" type="info"></v-alert>
    </v-container>
</template>


<script>
export default{
    name: 'AlertView',
    data(){
        return{
            alertState: false
        }
    }
}
</script>