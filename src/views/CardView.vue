<template>
    <v-container :fluid="true">
        <h1 class="text-green-darken-4">Card</h1>
        <v-row>
            <v-col>
                <!-- forma 1 -->
                <v-card width="400" title="Titulo 1" subtitle="subtitulo1" text="text"></v-card>
                <br>
                <!-- forma 2 -->
                <v-card width="400">
                    <v-card-item>
                        <v-card-title>Titulo 2</v-card-title>
                        <v-card-subtitle>Subtitulo 2</v-card-subtitle>
                    </v-card-item>
                    <v-card-text>texto</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>


<script>
export default{
    name: 'CardView'
}
</script>