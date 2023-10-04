<template>
    <v-container :fluid="true">
        <h1 class="text-green-darken-4">Formularios</h1>
        <v-row>
            <v-col>
                <!-- caja de texto -->
                <v-text-field label="Nombre" color="green" type="text" counter clearable maxLength="20" prepend-inner-icon="mdi-account">
                </v-text-field>
            </v-col>
            <v-col>
                <!-- lista de opciones (select en HTML) -->
                <v-select label="Pais" color="green" clearable :items="paises" item-title="pais" item-value="id" v-model="paisSeleccionado">
                </v-select>
            </v-col>
            <v-col>
                <!-- RadioButton -->
                <v-radio-group label="Departamento" v-model="departamento">
                    <v-radio color="green" label="San Salvador" value="San Salvador"></v-radio>
                    <v-radio color="green" label="Santa Ana" value="Santa Ana"></v-radio>
                    <v-radio color="green" label="San Miguel" value="San Miguel"></v-radio>
                </v-radio-group>
            </v-col>
            <v-col>
                <!-- checkboxes -->
                <v-checkbox color="green" label="Azul" value="Azul" v-model="colores"></v-checkbox>
                <v-checkbox color="green" label="Negro" value="Negro" v-model="colores"></v-checkbox>
                <v-checkbox color="green" label="Morado" value="Morado" v-model="colores"></v-checkbox>
            </v-col>
        </v-row>
        <h3>Datos</h3>
        Nombre:
        <p>{{ nombre }}</p>
        Pa&iacute;s:
        <p>{{ nombrePaisSeleccionado }}</p>
        Departamento:
        <p>{{ departamento }}</p>
        Colores:
        <p v-for="(color, i) in colores" :key="i">{{ color }}</p>
        <!-- botones -->
        <v-row>
            <v-col>
                <v-btn color="red">Bot&oacute;n 1</v-btn>
            </v-col>
            <v-col>
                <v-btn color="green" rounded="x1">Bot&oacute;n 2</v-btn>
            </v-col>
            <v-col>
                <v-btn color="indigo" variant="outlined">Bot&oacute;n 3</v-btn>
            </v-col>
            <v-col>
                <v-btn color="blue" prepend-icon="mdi-check">Guardar</v-btn>
            </v-col>
            <v-col>
                <v-btn color="purple" block append-icon="mdi-cancel">Camcelar</v-btn>
            </v-col>
        </v-row>
    </v-container>
</template>


<script>
export default{
    name: 'FormView',
    data(){
        return{
            paises: [
                {id: 1, pais: 'El Salvador'},
                {id: 2, pais: 'Guatemala'},
                {id: 3, pais: 'Honduras'}
            ],
            paisSeleccionado : 1,
            departamento: 'San Salvador',
            colores: ['Azul'],
            nombre: 'Israel Vasquez'
        }
    },
    computed: {
        nombrePaisSeleccionado() {
            const pais = this.paises.find(item => item.id === this.paisSeleccionado);
            return pais ? pais.pais : null;
        }
    }
}
</script>