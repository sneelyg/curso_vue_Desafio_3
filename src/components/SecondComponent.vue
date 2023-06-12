<template>
    <div class="principal">
        <TestComponent 
        active='false'
        subtitulo="Yashauuu" />
        <div class=" secundario">
            <p>{{ subtitulo }}</p>

            <table>
                <th>{{ titulo_tabla }}</th>
                <tr v-for="(elements) of datos" :key="elements">
                    <td>{{ elements * elements }}
                        <TestComponent 
                        active= 'true'
                        subtitulo="'Holaaaa'" />
                    </td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
import TestComponent from './TestComponent.vue';
export default {
    name: 'SecondComponent',
    props: {
        titulo: String,
        titulo_tabla: String,
        subtitulo: String,
        datos: Array,

    },
    components: { TestComponent }

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