<template>
    <div class=" md:w-[1050px] w-full h-full md:pt-[15px] pb-[100px] z-[2] relative">
        <!-- //News -->
        <div id="news-txt"
            class="bg-[#080808] text-white md:text-[50px] text-[30px] absolute md:top-[-65px] top-[-35px] md:left-0 left-[21px] pl-[20px] pr-[20px] font-bold rounded-[10px] ">
            <NuxtLink to="#">
                <h1 class="hover:text-[#ffcd43] transition-all ease-in-out duration-[300ms]">
                    NEWS
                </h1>
            </NuxtLink>

        </div>
        <div class="holder grid grid-cols-1 md:gap-[35px] gap-[15px] md:w-[1050px] w-full">
            <NuxtLink to="#" id="card" v-for="item in daata" :key="item.user_id" class="md:ml-[0] flex flex-col items-center justify-center
            w-full  md:h-[350px] h-[350px]">
                <div id="img"
                    class="md:w-full w-[90%] md:h-full h-[230px] bg-[#575757] rounded-tr-[10px] rounded-tl-[10px] flex items-center justify-center ">
                    <h1 class="text-[20px] text-white font-bold ">
                        Coming Soon !
                    </h1>
                </div>
                <div id="textForCard"
                    class=" bg-[#2c2c2c] md:h-[165px] h-[90px] text-white md:w-full w-[90%] rounded-br-[10px] rounded-bl-[10px] flex flex-col items-start justify-center p-[10px]">
                    <div class="txtHolder relative w-full h-full ">
                        <div
                            class=" absolute top-[5px] left-[5px] md:text-[20px] text-[15px] font-bold  mb-auto overflow-hidden truncate w-[95%]">
                            TITLE
                        </div>
                        <div
                            class="absolute bottom-[5px] left-[5px] md:text-[15px] text-[10px]  flex-col items-center w-full  pb-[5px]">
                            <h1 class="">
                                @{{ item.instagram }}
                            </h1>
                            <p class="md:text-[15px] text-[10px] mt-[1px]">
                                11-11-2023
                            </p>
                        </div>
                    </div>

                </div>
            </NuxtLink>
        </div>
        <!-- //News -->

        <!-- //current event -->
        <div id="current_event" class="w-full flex-col items-center md:mt-[100px] mt-[30px] flex">
            <div id="event-txt"
                class="text-white font-bold md:text-[50px] text-[30px] mb-[10px] md:mr=0 mr-auto md:ml-0 ml-[15px]">
                <NuxtLink to="#">
                    <h1 class="hover:text-[#ffcd43] transition-all ease-in-out duration-[300ms]">
                        On-going Event
                    </h1>
                </NuxtLink>
            </div>
            <div id="curr-event"
                class="md:w-full w-[90%] md:h-[450px] h-[300px] bg-[#575757] overflow-hidden relative rounded-[10px]">
                <div id="diagonal"
                    class="z-[2] absolute md:bottom-[-30px] bottom-[-150px] md:left-[-750px] left-[-390px] w-full h-[350px] bg-[#2c2c2c] rotate-45 transition-all ease-in-out duration-[200ms]">

                </div>
                <NuxtLink to="#">
                    <img id="img-event"
                        class="absolute z-[1] top-0 h-full w-full object-cover transition-all ease-in-out duration-[200ms]"
                        src="https://static.fandomspot.com/images/12/23540/00-featured-lol-original-rakan-splash-image.jpg"
                        alt="">
                    <div id="event-title-txt"
                        class="absolute md:bottom-[30px] bottom-[20px] md:left-[30px] left-[20px] z-[3] text-white font-semibold md:text-[50px] text-[30px] bg-[#2c2c2c] pr-[20px] transition-all ease-in-out duration-[200ms]">
                        <div class="flex items-center justify-center">
                            HYBRID
                        </div>
                    </div>
                </NuxtLink>
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

#curr-event:hover #diagonal,
#curr-event:hover #event-title-txt {
    background: #ffcd43;
    color: black;
}

#curr-event:hover #img-event {
    transform: scale(130%);
}</style>