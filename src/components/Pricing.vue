<template>
  <div class="bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mt-16 grid gap-8 lg:grid-cols-3">
        <div class="p-8 bg-white rounded-xl shadow-lg ring-1 ring-indigo-600">
          <h3 class="text-2xl font-bold tracking-tight text-gray-900">
            Basic Plan
          </h3>
          <p class="mt-6 text-base leading-7 text-gray-600">
            Lorem ipsum dolor sit amet consect etur adipisicing elit. Itaque
            amet indis perferendis blanditiis repellendus etur quidem assumenda.
          </p>
          <div class="mt-10 flex items-center gap-x-4">
            <h4
              class="flex-none text-sm font-semibold leading-6 text-indigo-600"
            >
              What’s included
            </h4>
            <div class="h-px flex-auto bg-gray-100"></div>
          </div>
          <ul
            role="list"
            class="mt-8 space-y-2 text-sm leading-6 text-gray-600"
          >
            <li
              v-for="feature in basicFeatures"
              :key="feature"
              class="flex items-center gap-x-3"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m4.5 12.75 6 6 9-13.5"
                />
              </svg>
              <span>{{ feature }}</span>
            </li>
          </ul>
          <div class="mt-8">
            <p class="text-3xl font-bold text-gray-900">$29</p>
            <p class="mt-2 text-sm text-gray-600">per month</p>
            <button
              class="mt-4 block w-full rounded-md bg-indigo-600 px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 focus:ring-offset-gray-100"
            >
              Select Plan
            </button>
          </div>
        </div>

        <div class="p-8 bg-white rounded-xl shadow-lg ring-1 ring-indigo-600">
          <h3 class="text-2xl font-bold tracking-tight text-gray-900">
            Premium Plan
          </h3>
          <p class="mt-6 text-base leading-7 text-gray-600">
            Lorem ipsum dolor sit amet consect etur adipisicing elit. Itaque
            amet indis perferendis blanditiis repellendus etur quidem assumenda.
          </p>
          <div class="mt-10 flex items-center gap-x-4">
            <h4
              class="flex-none text-sm font-semibold leading-6 text-indigo-600"
            >
              What’s included
            </h4>
            <div class="h-px flex-auto bg-gray-100"></div>
          </div>
          <ul
            role="list"
            class="mt-8 space-y-2 text-sm leading-6 text-gray-600"
          >
            <li
              v-for="feature in premiumFeatures"
              :key="feature"
              class="flex items-center gap-x-3"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m4.5 12.75 6 6 9-13.5"
                />
              </svg>
              <span>{{ feature }}</span>
            </li>
          </ul>
          <div class="mt-8">
            <p class="text-3xl font-bold text-gray-900">$49</p>
            <p class="mt-2 text-sm text-gray-600">per month</p>
            <button
              class="mt-4 block w-full rounded-md bg-indigo-600 px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 focus:ring-offset-gray-100"
            >
              Select Plan
            </button>
          </div>
        </div>

        <div class="p-8 bg-white rounded-xl shadow-lg ring-1 ring-indigo-600">
          <h3 class="text-2xl font-bold tracking-tight text-gray-900">
            Custom Plan
          </h3>
          <p class="mt-6 text-base leading-7 text-gray-600">
            Lorem ipsum dolor sit amet consect etur adipisicing elit. Itaque
            amet indis perferendis blanditiis repellendus etur quidem assumenda.
          </p>
          <div class="mt-10 flex items-center gap-x-4">
            <h4
              class="flex-none text-sm font-semibold leading-6 text-indigo-600"
            >
              What’s included
            </h4>
            <div class="h-px flex-auto bg-gray-100"></div>
          </div>
          <ul
            role="list"
            class="mt-8 space-y-2 text-sm leading-6 text-gray-600"
          >
            <li
              v-for="feature in customFeatures"
              :key="feature"
              class="flex items-center gap-x-3"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m4.5 12.75 6 6 9-13.5"
                />
              </svg>
              <span>{{ feature }}</span>
            </li>
          </ul>
          <div class="mt-8">
            <p class="text-3xl font-bold text-gray-900">$99</p>
            <p class="mt-2 text-sm text-gray-600">per month</p>
            <button
              class="mt-4 block w-full rounded-md bg-indigo-600 px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 focus:ring-offset-gray-100"
            >
              Select Plan
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PricingComponent",
  data() {
    return {
      basicFeatures: [
        "Feature 1",
        "Feature 2",
        "Feature 3",
        "Feature 4",
        "Feature 5",
      ],
      premiumFeatures: [
        "Feature 1",
        "Feature 2",
        "Feature 3",
        "Feature 4",
        "Feature 5",
      ],
      customFeatures: [
        "Feature 1",
        "Feature 2",
        "Feature 3",
        "Feature 4",
        "Feature 5",
      ],
    };
  },
};
</script>
