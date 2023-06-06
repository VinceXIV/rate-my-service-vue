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
    
</style>