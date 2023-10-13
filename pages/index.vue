<template>
    <div  class ="h-full w-full md:w- flex flex-col items-center bg-[#080808]">  
        <div class="w-full md:w-full flex flex-col items-center">
            <!-- <navbarr/> -->
            <Hero/>
            <main_content/>
            <foooter/>
        </div>
    </div>
</template>

<script setup>

</script>

<style>
html, body {
    height: 101%;
}

/* width */
::-webkit-scrollbar {
  width: 5px;
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