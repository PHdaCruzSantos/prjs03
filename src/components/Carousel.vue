<template>
  <div
    class="block h-96 overflow-hidden content-normal pr-7 pl-7 pb-3 pt-3 relative"
  >
    <div class="flex overflow-hidden relative">
      <div
        v-for="(service, index) in services"
        :key="index"
        class="flex justify-center w-full carousel-slide mt-4 mb-4"
        :style="{ transform: `translateX(-${currentOffset}%)` }"
      >
        <div
          class="bg-white rounded-lg overflow-hidden shadow-lg transition duration-500 ease-in-out transform hover:-translate-y-1 ring-1 ring-indigo-600"
        >
          <img
            :src="service.image"
            :alt="service.title"
            class="w-full h-64 object-cover"
          />
          <div class="p-4">
            <h3 class="text-xl font-semibold text-indigo-800">
              {{ service.title }}
            </h3>
            <p class="mt-2 text-gray-600">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </div>
    <button
      class="prev absolute w-10 h-10 bg-slate-400 rounded-full ring-1 ring-indigo-600 transition duration-500 ease-in-out tranform hover:scale-110 hover:bg-indigo-600 text-indigo-600 hover:text-white"
      @click="prevSlide"
      :class="{ hidden: currentOffset === 0 }"
    >
      <span class="">&#10094;</span>
    </button>
    <button
      class="next absolute w-10 h-10 bg-slate-400 rounded-full ring-1 ring-indigo-600 transition duration-500 ease-in-out tranform hover:scale-110 hover:bg-indigo-600 text-indigo-600 hover:text-white"
      @click="nextSlide"
      :class="{
        hidden: currentSlide >= services.length * 2,
      }"
    >
      <span class="">&#10095;</span>
    </button>
  </div>
</template>

<script>
export default {
  name: "ServiceCards",
  data() {
    return {
      services: [
        {
          id: 1,
          title: "Service 1",
          description: "Description for Service 1",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 2,
          title: "Service 2",
          description: "Description for Service 2",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 3,
          title: "Service 3",
          description: "Description for Service 3",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 4,
          title: "Service 4",
          description: "Description for Service 4",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 5,
          title: "Service 5",
          description: "Description for Service 5",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 6,
          title: "Service 6",
          description: "Description for Service 6",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 7,
          title: "Service 7",
          description: "Description for Service 7",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 8,
          title: "Service 8",
          description: "Description for Service 8",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 9,
          title: "Service 9",
          description: "Description for Service 9",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 10,
          title: "Service 10",
          description: "Description for Service 10",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 11,
          title: "Service 11",
          description: "Description for Service 11",
          image: "https://via.placeholder.com/400x300",
        },
        {
          id: 12,
          title: "Service 12",
          description: "Description for Service 12",
          image: "https://via.placeholder.com/400x300",
        },
      ],
      currentOffset: 0,
      currentSlide: 0,
    };
  },
  methods: {
    nextSlide() {
      if (this.currentOffset === this.services.length - 3) return;
      this.currentOffset += 100;
      this.currentSlide += 3;
      console.log("nextSlide: ", this.currentSlide);
      console.log("services.length: ", this.services.length);
    },
    prevSlide() {
      if (this.currentOffset === 0) return;
      this.currentOffset -= 100;
      this.currentSlide -= 3;
      console.log("prevSlide: ", this.currentSlide);
    },
    goToSlide(index) {
      this.currentOffset = index * (100 / 3);
      this.currentSlide = index * 3;
    },
  },
};
</script>

<style scoped>
.carousel-slide {
  flex: 0 0 calc(100% / 3);
  transition: transform 0.5s ease;
}

.prev,
.next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  border: none;
  cursor: pointer;
  font-size: 24px;
}

.prev {
  left: 10px;
}

.next {
  right: 10px;
}
</style>
