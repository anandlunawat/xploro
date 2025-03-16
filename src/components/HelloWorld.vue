<template>
  <div class="font-rubik text-[#100B21]">
    <!-- Hero Section with Background -->
    <div class="relative flex flex-col h-96">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <img src="../assets/bg.jpg" class="z-50 object-fill w-full h-full md:object-cover" />
      </div>
      <div class="absolute inset-0 bg-[#0000006d]"></div>

      <!-- Overlay (Optional for better readability) -->

      <!-- Navbar -->
      <nav class="relative z-10 flex items-center justify-between p-4 text-white">
        <h1 class="font-extrabold text-white md:text-4xl">Xploro</h1>
        <!-- <input type="text" placeholder="Search destination..." class="w-full p-2 text-black rounded md:w-1/2"> -->
        <button class="px-4 py-2 font-semibold md:text-[20px] text-white bg-[#0204037e] rounded">Login</button>
      </nav>

      <!-- Hero Section -->
      <section class="relative z-10 flex flex-col items-center justify-center h-full px-4 text-white">
        <h2 class="text-3xl font-bold text-white md:text-5xl">Plan Your Next Journey</h2>
        <!-- <p class="mt-2 text-lg">Flights | Hotels | Trains | Cabs</p> -->
      </section>
    </div>

    <!-- Trending Destinations -->
    <section class="p-4 bg-white md:p-8">
      <h3 class="mb-4 text-2xl font-semibold">Trending Destinations</h3>
      <div class="grid grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-4">
        <div v-for="(destination, index) in destinations" :key="index" class="p-4 bg-gray-100 rounded shadow-lg">
          <img :src="destination.image" class="object-cover w-full h-40 rounded" />
          <h4 class="mt-2 text-lg font-semibold">{{ destination.name }}</h4>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="p-4 mt-4 text-center text-white bg-gray-900">
      <p>&copy; 2025 Xploro. All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      destinations: [
        { name: "Goa", image: "https://source.unsplash.com/400x300/?beach" },
        { name: "Manali", image: "https://source.unsplash.com/400x300/?mountains" },
        { name: "Jaipur", image: "https://source.unsplash.com/400x300/?fort" },
        { name: "Kerala", image: "https://source.unsplash.com/400x300/?backwaters" }
      ]
    };
  }
};
</script>
