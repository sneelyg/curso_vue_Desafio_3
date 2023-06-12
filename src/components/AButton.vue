<template>
    <button class="btn"  @click="handleClick">
        Click
    </button>
</template>

<script>

export default {
    name: "AButton",
    props: {
       
    },
    methods:{
        handleClick(){
            console.log("Clock en el hijo")
            this.$emit('clickHijo')
        }


    }

}

</script>


<style scoped>
.btn{
    background-color: green;
    color: white;
    border: none;
    border-radius: 5px;
}

</style>