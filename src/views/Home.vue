<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script>
import { Options, Vue } from "vue-class-component";
import HelloWorld from "src/components/HelloWorld.vue"; 
import { defineComponent } from "vue";

export default {
  components: {
    HelloWorld
  }
}

</script>
