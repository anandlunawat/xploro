<template>
  <div class="font-sans">
    <!-- Navbar -->
    <nav class="flex items-center justify-between p-4 text-white bg-red-600">
      <h1 class="text-xl font-bold">MakeMyTrip Clone</h1>
      <button class="px-4 py-2 text-red-600 bg-white rounded">Login</button>
    </nav>

    <!-- Hero Section -->
    <section class="flex flex-col items-center justify-center px-4 text-white bg-center bg-cover h-80 md:px-0" 
      style="background-image: url('https://source.unsplash.com/1600x900/?travel');">
      <h2 class="text-3xl font-bold md:text-5xl">Book Your Next Journey</h2>
      <p class="mt-2 text-lg">Flights | Hotels | Trains | Cabs</p>
      <input type="text" placeholder="Search destination..." class="w-full p-2 mt-4 text-black rounded md:w-1/2">
    </section>

    <!-- Trending Destinations -->
    <section class="p-4 md:p-8">
      <h3 class="mb-4 text-2xl font-semibold text-red-600">Trending Destinations</h3>
      <div class="grid grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-4">
        <div v-for="(destination, index) in destinations" :key="index" class="p-4 bg-gray-100 rounded shadow-lg">
          <img :src="destination.image" class="object-cover w-full h-40 rounded" />
          <h4 class="mt-2 text-lg font-semibold text-red-600">{{ destination.name }}</h4>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="p-4 mt-4 text-center text-white bg-gray-900">
      <p>&copy; 2025 MakeMyTrip Clone. All rights reserved.</p>
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

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
