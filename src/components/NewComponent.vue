<template>
    <div class="principal">
    
        <h3>{{ titulo }}</h3>
        <div class=" secundario">
            <p>{{ subtitulo }}</p>

            <table>
                <th>{{ titulo_tabla }}</th>
                <tr v-for="(elements) of datos" :key="elements">
                    <td>{{ elements }}</td>
                </tr>
            </table>

        </div>
    </div>
</template>

<script>



export default {
    name: "NewComponent",
    props: {
        titulo: String,
        titulo_tabla: String,
        subtitulo: String,
        datos: Array,
    },

}
</script>

<style scoped>
.principal {
    background-color: lightgreen;
    color: darkblue;
    margin: 25px 25px 25px 25px;
    padding: 25px 25px 25px 25px;
}

.secundario {
    background-color: green;
    color: darkred;
    margin: 25px 25px 25px 25px;
    padding: 25px 25px 25px 25px;

}
</style>