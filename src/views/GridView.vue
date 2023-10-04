<template>
    <v-container :fluid="true">
        <h1 class="text-green-darken-4">Grid</h1>

        <!-- filas -->
        <v-row>
            <!-- columnas -->
            <v-col>Columna 1</v-col>
            <v-col>Columna 2</v-col>
            <v-col>Columna 3</v-col>
        </v-row>

        <v-row>
            <v-col class="bg-blue-lighten-4 text-indigo">Columna 4</v-col>
        </v-row>

        <v-row>
            <v-col cols="7" class="bg-purple">Columna 5</v-col>
            <v-col cols="3">Columna 6</v-col>
            <v-col cols="2" class="bg-indigo">Columna 7</v-col>
        </v-row>
        

    </v-container>
</template>


<script>
export default{
    name: 'GridView'
}
</script>