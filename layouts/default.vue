<template>
    <div class="w-full bg-black sticky top-0 flex items-center justify-center z-[10]">
        <div
            class="md:w-[1050px] w-full h-[85px] md:h-[105px] flex flex-col items-center justify-center bg-black text-white ">
            <div class="w-full h-[40px] flex items-center  md:pt-[25px] md:pr-0 md:pl-0 ">
                <div class="text flex items-center h-full md:pl-[0px] pl-[15px]">
                    <NuxtLink to="/">
                        <h1 class=" text-[35px] font-bold">
                            Academy Digi/Tradi Arts Indonesia
                        </h1>
                    </NuxtLink>
                </div>

                <!-- <div class="searchbar flex items-center md:hidden
                border-1[px] ml-auto border-black border-solid rounded-[100px]">
                    <button>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5"
                            class="w-8 h-8 pl-[10px]" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
                        </svg>
                    </button>
                </div> -->

                <!-- <div class="searchbar hidden
            w-[350px] h-[40px] ml-[20px] md:flex items-center bg-white
            rounded-[100px]">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        class="w-6 h-6 pl-[10px] stroke-[#a1a09d]">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
                    </svg>
                    <input type="text" placeholder="search"
                        class="pl-[5px] text-[#a1a09d] w-full h-full rounded-[100px] focus:outline-none active:border-none">
                </div> -->

                <div class="ml-[10px] md:hidden flex items-center">
                    <button>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2"
                            stroke="currentColor" class="w-8 h-8">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                        </svg>

                    </button>
                </div>

                <div class="signIn hidden md:flex items-center ml-auto hover:text-[#ffcd43] duration-[200ms]">
                    <NuxtLink to="/login" class="flex items-center justify-center">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15m3 0l3-3m0 0l-3-3m3 3H9" />
                        </svg>
                        <h1 class="ml-[5px]">
                            Login
                        </h1>
                    </NuxtLink>
                </div>

                <div id="langOpt"
                    class="relative text-center ml-[20px] hidden md:flex items-center justify-center   hover:text-[#ffcd43]">
                    <button id="dick" class=" h-[30px] text-center flex items-center justify-center">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" class="w-6 h-6 duration-[200ms]">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M10.5 21l5.25-11.25L21 21m-9-3h7.5M3 5.621a48.474 48.474 0 016-.371m0 0c1.12 0 2.233.038 3.334.114M9 5.25V3m3.334 2.364C11.176 10.658 7.69 15.08 3 17.502m9.334-12.138c.896.061 1.785.147 2.666.257m-4.589 8.495a18.023 18.023 0 01-3.827-5.802" />
                        </svg>

                        <h1 class="ml-[5px] duration-[200ms]">
                            Language
                        </h1>

                        <svg id="langArrow" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                            stroke-width="1.5" stroke="currentColor" class="w-5 h-5 ml-[5px]">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
                        </svg>
                    </button>

                    <div id="dropdownlang"
                        class="h-[0px] w-[123px] absolute flex-col items-center justify-center top-[30px] z-[2] bg-[#4d4d4d] transition-all ease-out duration-[300ms] text-white font-semibold flex ">
                        <div class="hover:bg-[#2c2c2c] w-full h-full transition-all ease-in-out duration-[.3s]">
                            <NuxtLink id="langopt" to="#"
                                class="flex justify-center items-center opacity-0 transition-all ease-in w-full h-full">
                                <h1 class=" hover:bg-[#2c2c2c] transition-all ease-in-out duration-[100ms]">
                                    English
                                </h1>
                            </NuxtLink>
                        </div>

                        <div class="hover:bg-[#2c2c2c] w-full h-full transition-all ease-in-out duration-[.3s]">
                            <NuxtLink id="langopt" to="#"
                                class=" flex justify-center items-center opacity-0 transition-all ease-in w-full h-full ">
                                <h1 class=" transition-all ease-in-out duration-[100ms] ">
                                    日本語
                                </h1>
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>



            <div id="links" class="w-full h-[20px] mt-auto mb-[15px] flex relative">
                <!-- <div id="categories" class="hidden md:flex items-center justify-center">
                    <button class="flex justify-center items-center">
                        <svg id="catArrow" :class="{ catClicked: cat_state }" xmlns="http://www.w3.org/2000/svg" fill="none"
                            viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                            class="w-6 h-6 transition-all ease-in-out">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
                        </svg>

                        <h1 class="ml-[7px]">
                            Categories
                        </h1>
                    </button>
                    <div id="categoriesDrop"
                        class=" absolute w-full top-[22px] right-0 h-[0px] border-white transition-all ease delay-[20ms] flex flex-col items-center justify-start bg-black">
                        <div id="catList"
                            class="w-full mt-[15px] hidden grid-cols-6 gap-[50px] items-center justify-center overflow-hidden"
                            :class="{ catToggle: cat_state }">
                            <div class="cat01 flex flex-col h-full">
                                <h1 class=" font-bold border-b-[1px] mb-[10px]">
                                    Illustration
                                </h1>
                                <ul>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Anatomy</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Character</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Concept Art</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Background</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Comic</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Animations/3D</li>
                                </ul>
                            </div>
                            <div class="cat02 h-full">
                                <h1 class="font-bold border-b-[1px] mb-[10px]">
                                    Media Design
                                </h1>
                                <ul>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">2D</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">3D</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">VFX</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Blender</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Animation</li>
                                </ul>
                            </div>
                            <div class="cat03 h-full">
                                <h1 class="font-bold border-b-[1px] mb-[10px]">
                                    Design
                                </h1>
                                <ul>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Graphic Design</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Brand Design</li>
                                </ul>
                            </div>
                            <div class="cat04 h-full">
                                <h1 class="font-bold border-b-[1px] mb-[10px]">
                                    Food
                                </h1>
                                <ul>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Pastry</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Bakery</li>
                                </ul>
                            </div>
                            <div class="cat05 h-full">
                                <h1 class="font-bold border-b-[1px] mb-[10px]">
                                    Beauty
                                </h1>
                                <ul>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Hair</li>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">Cosmetic</li>
                                </ul>
                            </div>
                            <div class="cat06 h-full">
                                <h1 class="font-bold border-b-[1px] mb-[10px]">
                                    Career Dev.
                                </h1>
                                <ul>
                                    <li class="ml-[10px] text-ellipsis overflow-hidden ...">IT</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div> -->

                <NuxtLink to="/" class="md:ml-0 ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    Home
                </NuxtLink>
                <NuxtLink to="/freeClasses"
                    class="ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    News
                </NuxtLink>
                <NuxtLink to="/best" class="ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    Event
                </NuxtLink>
                <NuxtLink to="/whatsNew" class="ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    Guides
                </NuxtLink>
                <NuxtLink to="/whatsNew" class="ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    Members
                </NuxtLink>
                <NuxtLink to="/event" class="ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    About Us
                </NuxtLink>
                <NuxtLink to="b2b" class="ml-[15px] hover:text-[#ffcd43] transition-all ease-in-out duration-[200ms]">
                    Join Us
                </NuxtLink>
            </div>

            <!-- <div id="categoriesDrop"
                class="categories absolute top-[105px] mb-[20px] w-full h-[0px]  transition-all ease delay-[20ms] flex flex-col items-center justify-start bg-black">
                <div id="catList" class="w-[1250px] mt-[10px] hidden grid-cols-6 gap-[50px] overflow-hidden items-center"
                    :class="{ catToggle: cat_state }">
                    <div class="cat01 flex flex-col h-full">
                        <h1 class=" font-bold border-b-[1px] mb-[10px]">
                            Illustration
                        </h1>
                        <ul>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Anatomy</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Character</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Concept Art</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Background</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Comic</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Animations/3D</li>
                        </ul>
                    </div>
                    <div class="cat02 h-full">
                        <h1 class="font-bold border-b-[1px] mb-[10px]">
                            Media Design
                        </h1>
                        <ul>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">2D</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">3D</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">VFX</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Blender</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Animation</li>
                        </ul>
                    </div>
                    <div class="cat03 h-full">
                        <h1 class="font-bold border-b-[1px] mb-[10px]">
                            Design
                        </h1>
                        <ul>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Graphic Design</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Brand Design</li>
                        </ul>
                    </div>
                    <div class="cat04 h-full">
                        <h1 class="font-bold border-b-[1px] mb-[10px]">
                            Food
                        </h1>
                        <ul>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Pastry</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Bakery</li>
                        </ul>
                    </div>
                    <div class="cat05 h-full">
                        <h1 class="font-bold border-b-[1px] mb-[10px]">
                            Beauty
                        </h1>
                        <ul>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Hair</li>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">Cosmetic</li>
                        </ul>
                    </div>
                    <div class="cat06 h-full">
                        <h1 class="font-bold border-b-[1px] mb-[10px]">
                            Career Dev.
                        </h1>
                        <ul>
                            <li class="ml-[10px] text-ellipsis overflow-hidden ...">IT</li>
                        </ul>
                    </div>
                </div>
            </div> -->

        </div>
    </div>

    <!-- content output -->
    <div>
        <slot />
    </div>
    <!-- content output -->
</template>

<script>
export default {
    data() {
        return {
            cat_state: false,
            lang_state: false
        }
    }
    ,
    methods: {
        toggle_cat() {
            if (this.cat_state == false) {
                document.getElementById('categoriesDrop').style.height = "200px";
                this.cat_state = !this.cat_state;
                console.log("cheese");
            } else {
                document.getElementById('categoriesDrop').style.height = "0px";
                this.cat_state = !this.cat_state;
                console.log("cheeseww");
            }
        }
        ,
        toggle_lang() {
            if (this.lang_state == false) {
                document.getElementById('dropdownlang').style.display = "flex";
                this.lang_state = !this.lang_state;
                console.log("cheese");
            } else {
                document.getElementById('dropdownlang').style.display = "none";
                this.lang_state = !this.lang_state;
                console.log("cheeseww");
            }
        }
    }
}
</script>

<style scoped>
#categories:hover #categoriesDrop {
    height: 220px;
}

#categories:hover #categoriesDrop #catList {
    display: flex;
}

#langArrow {
    transform: rotate(0deg);
    transition: all 200ms ease-in-out;
}

#langOpt:hover #langArrow {
    transform: rotate(180deg);
    transition: all 200ms ease-in-out;
}

#langOpt:hover #dropdownlang {
    height: 70px;
}

#langOpt:hover #dropdownlang #langopt {
    visibility: visible;
    opacity: 1.0;
    transition-delay: 0ms, 250ms;
}

.catToggle {
    display: grid;
}

.catClicked {
    transform: rotate(180deg);
    transition: all 0.3s ease-in-out;
}

.langClicked {
    transform: rotate(180deg);
    transition: all 0.3s ease-in-out;
}

#catArrow {
    transition: all 0.3s ease-in-out;
}

#links .router-link-active {
    color: rgb(246, 248, 99);
}</style>