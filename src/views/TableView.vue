<template>
    <v-container :fluid="true">
        <h1 class="text-green-darken-4">Table</h1>
        <v-table hover>
            <thead>
                <tr>
                    <th>Nombres</th>
                    <th>Apellidos</th>
                    <th>Acciones</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Israel</td>
                    <td>Vasquez</td>
                    <td><v-btn icon="mdi-close" size="small" color="red"></v-btn></td>
                </tr>
                <tr>
                    <td>Chico</td>
                    <td>Flores</td>
                    <td><v-btn icon="mdi-pencil" size="small" color="indigo"></v-btn></td>
                </tr>
            </tbody>
        </v-table>
    </v-container>
</template>


<script>
export default{
    name: 'TableView'
}
</script>