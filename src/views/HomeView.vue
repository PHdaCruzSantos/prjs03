<template>
  <div class="home">
    <h1>This is an home page</h1>
    <CarouselComponent />
  </div>
</template>

<script>
import CarouselComponent from "../components/Carousel.vue";
export default {
  name: "HomeView",
  components: {
    CarouselComponent,
  },
};
</script>
