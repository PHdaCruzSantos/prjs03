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
  data() {
    return {
      carouselSlides: [
        {
          id: 1,
          src: "https://via.placeholder.com/400x300",
          alt: "Service 1",
        },
        {
          id: 2,
          src: "https://via.placeholder.com/400x300",
          alt: "Service 2",
        },
        {
          id: 3,
          src: "https://via.placeholder.com/400x300",
          alt: "Service 3",
        },
      ],
    };
  },
};
</script>
<!-- <style scoped>
.carousel {
  position: relative;
  max-height: 100vh;
  height: 100vh;
}

.carousel .slide-info {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  max-height: 100%;
  height: 100%;
}

.carousel .slide-info img {
  min-width: 100%;
  height: 100%;
  object-fit: cover;
}
</style> -->
