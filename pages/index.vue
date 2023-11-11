<template>
    <div  class ="h-full w-full md:w- flex flex-col items-center bg-[#080808]">  
        <div class="w-full md:w-full flex flex-col items-center">
            <!-- <navbarr/> -->
            <Hero/>
            <Dashboard/>
            <New_artwork/>
            <!-- <foooter/> -->
        </div>
    </div>
</template>

<script setup>
import New_artwork from './new_artwork.vue';
import Dashboard from './Dashboard.vue';

</script>

<style>
/* html, body {
    height: 101%;
} */

/* width */
::-webkit-scrollbar {
  width: 5px;
  /* height: 10px; */
}

/* Track */
::-webkit-scrollbar-track {
  background: #494949;
}

/* Handle */
::-webkit-scrollbar-thumb {
    border-radius: 100px;
  background: #a8a8a8;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>