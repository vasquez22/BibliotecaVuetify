<template>
    <v-container :fluid="true">
        <h1 class="text-green-darken-4">Tabs</h1>
        <!-- pestañas -->
        <v-tabs v-model="tabs" bg-color="teal-darken-4">
        <v-tab value="1">Tab 1</v-tab>
        <v-tab value="2">Tab 2</v-tab>
        <v-tab value="3">Tab 3</v-tab>
        </v-tabs>

        <!-- contenido de las ventanas -->
        <v-window v-model="tabs">
        <v-window-item value="1">Contenido de pestaña 1</v-window-item>
        <v-window-item value="2">Contenido de pestaña 2</v-window-item>
        <v-window-item value="3">Contenido de pestaña 3</v-window-item>
        </v-window>
    </v-container>
</template>


<script>
export default{
    name: 'TabsView',
    data(){
        return{
            tabs: null
        }
    }
}
</script>