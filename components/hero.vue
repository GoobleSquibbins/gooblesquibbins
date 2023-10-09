<template>
    <div class="w-full h-[400px] ">
        <div class="hero w-full h-[350px] flex flex-col items-center justify-center">
            <img src="https://images7.alphacoders.com/116/1168975.png" class="heroImg absolute top-[105px] h-[400px] w-full">
        </div>
        <h1 class="absolute top-[350px] left-[30px] text-white text-[70px] font-bold border-b-[7px] border-white drop-shadow-lg">
            ウルトラキル
        </h1>
    </div>
</template>

<script setup>

</script>

<style scoped>
.heroImg {
    -webkit-mask-image: linear-gradient(#080808, transparent);
    mask-image: linear-gradient(#080808, transparent);
    object-fit: cover;
}
</style>