<template>
  <div class="font-rubik text-[#01090D]">
    <!-- Hero Section with Background -->
    <div class="relative flex flex-col md:h-[600px] h-[220px]">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <img
          src="../assets/bg.jpg"
          class="z-50 object-fill w-full h-full md:object-cover"
        />
      </div>
      <div class="absolute inset-0 bg-[#0000006d]"></div>

      <!-- Overlay (Optional for better readability) -->

      <!-- Navbar -->
      <nav
        class="relative z-10 flex items-center justify-between p-4 text-white"
      >
        <h1 class="font-extrabold text-white md:text-4xl">Xploro</h1>
        <!-- <input type="text" placeholder="Search destination..." class="w-full p-2 text-black rounded md:w-1/2"> -->
        <button
          class="px-4 py-2 font-semibold md:text-[20px] text-white bg-[#0204037e] rounded"
        >
          Login
        </button>
      </nav>

      <!-- Hero Section -->
      <div
        class="relative flex flex-row z-10 self-center md:gap-12 gap-2.5 justify-center p-4 text-center bg-white rounded-[8px] w-fit"
      >
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
        <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/flight.png"/>
          <h2>Flights</h2>
        </button>
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
        <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/hotels.png"/>
          Hotels
        </button>
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
          <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/villas_1.png"/>
          Homestays & Villas
        </button>
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
        <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/holiday.png"/>
          Holiday Packages
        </button>
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
        <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/train.png"/>
          Trains
        </button>
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
        <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/bus.png"/>
          Buses
        </button>
        <button
          class="text-[10px] hover:border-b-4 hover:border-b-[#305171] w-min hover:text-[#305171] flex flex-col font-extralight md:text-[25px]"
        >
        <img class="w-[30px] md:w-[70px] md:h-[70px] h-[30px]" src="../assets/cab.png"/>
          Cabs
        </button>
        <!-- <p class="mt-2 text-lg">Flights | Hotels | Trains | Cabs</p> -->
      </div>
    </div>

    <!-- Trending Destinations -->
    <section class="p-4 bg-white mb-14 md:p-8">
      <h3 class="mb-4 text-2xl font-semibold">Trending Destinations</h3>
      <div class="grid grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-4">
        <div
          v-for="(destination, index) in destinations"
          :key="index"
          class="p-4 bg-gray-100 rounded shadow-lg"
        >
          <img
            src="../assets/goa.jpg"
            class="w-full h-40 rounded object-full"
          />
          <h4 class="mt-2 text-lg font-semibold">{{ destination.name }}</h4>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <div
      class="-z-40 fixed bottom-0 w-[100vw] p-4 mt-10 text-center text-white bg-gray-900"
    >
      <p>&copy; 2025 Xploro. All rights reserved.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      destinations: [
        { name: "Goa", image: "../assets/goa.jpg" },
        {
          name: "Manali",
          image: "https://source.unsplash.com/400x300/?mountains",
        },
        { name: "Jaipur", image: "https://source.unsplash.com/400x300/?fort" },
        {
          name: "Kerala",
          image: "https://source.unsplash.com/400x300/?backwaters",
        },
      ],
    };
  },
};
</script>
