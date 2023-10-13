<template>
    <div class=" md:w-[1050px] w-full h-full mt-[10px] pb-[100px]">
        <div class="holder grid grid-cols-3 gap-[50px] w-[1050px]">
            <NuxtLink to="#" id="card" v-for="item in daata" :key="daata.user_id" class="flex flex-col items-center
            w-full h-[350px] ">
                <div id="img"
                    class="w-full h-full bg-[#575757] rounded-tr-[10px] rounded-tl-[10px] flex items-center justify-center">
                    <h1 class="text-[20px] text-white font-bold">
                        Coming Soon !
                    </h1>
                </div>
                <div id="textForCard"
                    class=" bg-[#2c2c2c] h-[165px] w-full rounded-br-[10px] rounded-bl-[10px] flex flex-col items-start justify-center p-[10px]">
                    <div class="txtHolder relative w-full h-full">
                        <h1 class=" absolute top-[5px] left-[5px] text-[20px] font-bold text-[white] mb-auto">
                            Piece Name
                        </h1>
                        <div class="absolute bottom-[5px] left-[5px] flex items-center w-full text-white pb-[5px]">
                            <h1 class="">
                                @{{ item.instagram }}
                            </h1>
                        </div>
                    </div>

                </div>
            </NuxtLink>
        </div>

    </div>
</template>

<script setup lang="ts">
const supabase = useSupabaseClient()

const { data: daata } = await useAsyncData('daata', async () => supabase.from('tbl_user').select('*').order('user_id'), { transform: result => result.data })

console.log(daata.value)
</script>

<style scoped>
#card {
    transition: all ease-in-out .3s;
}

#card:hover {
    transform: translatey(-20px);
}
</style>