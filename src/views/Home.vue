<template>
  <div class="home center">
    <camera />
  </div>
</template>

<script>
// @ is an alias to /src
import Camera from "@/components/Camera.vue";

export default {
  name: "home",
  components: {
    Camera
  }
};
</script>
