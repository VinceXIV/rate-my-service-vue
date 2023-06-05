<template>
  <div class="container">
      <div class="target" ref="target">Vue Moveable</div>
      <Moveable
          className="moveable"
          v-bind:target="['.target']"
          v-bind:draggable="true"
          v-bind:scalable="true"
          v-bind:rotatable="true"
          @drag="onDrag"
          @scale="onScale"
          @rotate="onRotate"
      />
  </div>
</template>
  <script>
  import Moveable from "vue3-moveable";
  
  export default {
    name: "MoveAble",
    components: {
      Moveable,
    },
    methods: {
      onDrag({ transform }) {
          this.$refs.target.style.transform = transform;
      },
      onScale({ drag }) {
          this.$refs.target.style.transform = drag.transform;
      },
      onRotate({ drag }) {
          this.$refs.target.style.transform = drag.transform;
      },
    }
  }
</script>

<style>
  .target {
    width: 10rem;
    margin: auto;
    margin-top: 10rem;
  }
</style>