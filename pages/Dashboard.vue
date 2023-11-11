<template>
    <div class=" md:w-[1050px] w-full h-full md:pt-[15px] pb-[100px] z-[2] relative">
        <!-- //News -->
        <div id="news-txt"
            class="bg-[#080808] text-white text-[50px] absolute top-[-70px] pl-[20px] pr-[20px] font-bold rounded-[10px] ">
            <NuxtLink to="#">
                <h1 class="hover:text-[#ffcd43] transition-all ease-in-out duration-[300ms]">
                    NEWS
                </h1>
            </NuxtLink>

        </div>
        <div class="holder grid grid-cols-1 md:gap-[35px] gap-[15px] md:w-[1050px] w-full">
            <NuxtLink to="#" id="card" v-for="item in daata" :key="item.user_id" class="md:ml-[0] flex flex-col items-center justify-center
            w-full  md:h-[350px] h-[250px]">
                <div id="img"
                    class="md:w-full w-[90%] md:h-full h-[130px] bg-[#575757] rounded-tr-[10px] rounded-tl-[10px] flex items-center justify-center ">
                    <h1 class="text-[20px] text-white font-bold ">
                        Coming Soon !
                    </h1>
                </div>
                <div id="textForCard"
                    class=" bg-[#2c2c2c] md:h-[165px] h-[100px] text-white md:w-full w-[90%] rounded-br-[10px] rounded-bl-[10px] flex flex-col items-start justify-center p-[10px]">
                    <div class="txtHolder relative w-full h-full ">
                        <h1 class=" absolute top-[5px] left-[5px] text-[20px] font-bold  mb-auto">
                            TITLE
                        </h1>
                        <div class="absolute bottom-[5px] left-[5px] flex-col items-center w-full  pb-[5px]">
                            <h1 class="">
                                @{{ item.instagram }}
                            </h1>
                            <p>
                                11-11-2023
                            </p>
                        </div>
                    </div>

                </div>
            </NuxtLink>
        </div>
        <!-- //News -->

        <!-- //current event -->
        <div id="current_event" class="w-full flex-col items-center mt-[100px]">
            <div id="event-txt" class="text-white font-bold text-[50px] mb-[30px]">
                <NuxtLink to="#">
                    <h1 class="hover:text-[#ffcd43] transition-all ease-in-out duration-[300ms]">
                        On-going Event
                    </h1>
                </NuxtLink>
            </div>
            <div id="curr-event" class="w-full h-[400px] bg-[#575757] overflow-hidden relative">
                <div id="diagonal" class="z-[2] absolute top-[30px] left-[-750px] w-full h-[350px] bg-[#2c2c2c] rotate-45">

                </div>
                <img class="absolute z-[1] top-0 h-full w-full object-cover"
                    src="https://static.fandomspot.com/images/12/23540/00-featured-lol-original-rakan-splash-image.jpg"
                    alt="">
                <div id="event-title-txt" class="absolute rounded-[10px] bottom-[30px] left-[50px] z-[3] text-white font-semibold text-[50px] bg-[#2c2c2c] pr-[20px]">
                    <h1>
                        HYBRID
                    </h1>
                </div>
            </div>
        </div>
        <!-- //current event -->

    </div>
</template>

<script setup lang="ts">
const supabase = useSupabaseClient()

interface YourDataType {
    user_id: number;
    instagram: string;
}

const { data, error } = await useAsyncData('daata', async () => supabase
    .from('tbl_user')
    .select('*')
    .limit(3)
    .order('user_id'), { transform: result => result.data })

const daata: YourDataType[] = data || [];

console.log(daata)
console.log(data)
console.log(error)
</script>

<style scoped>
#card {
    transition: all ease-in-out .3s;
}

#textForCard {
    transition: all ease-in-out 200ms;
}

#card:hover #textForCard {
    background-color: #ffcd43;
    color: black;
    transition: all ease-in-out 200ms;
}
</style>