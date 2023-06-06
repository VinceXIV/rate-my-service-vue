<template>
    <div class="canvas" v-for="object in objectArray" :key="object.id">
        <Moveable  v-bind:object="object"/>
    </div>
</template>

<script>
    import Moveable from "../../utilities/interactive/MoveAble/MoveAble.vue"

    export default {
        name: 'CanvasObject',
        props: {
            objectArray: Array
        },
        components: {
            Moveable
        }
    }   
</script>

<style>
    .canvas {
        position: relative;
        width: 50rem;
        height: 30rem;
        background-color: #d4d4d4;
        margin: auto;
        margin-top: 6rem;
        margin-right: 5rem
    }
</style>