<template>
<div>
    <h1 :class=" active? 'activo' : '' ">
        Howdy
    </h1>
    <h2>{{ subtitulo }}</h2>
</div>

</template>

<script>

export default {
    name: "TestComponent",
    props: {
        titulo: String,
        titulo_tabla: String,
        subtitulo: String,
        datos: Array,
        active: Boolean
    },

}
</script>


<style scoped>
.activo{
    background-color: black;
    color: yellow;
}

</style>