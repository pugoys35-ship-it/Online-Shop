<script>
export default {
    data() {
        return {
            backgroundHome: '',
        }
    },
    methods: {

    },
}
</script>

<template>

    <section class="relative">
        <div class="w-full h-screen  z-10 absolute flex flex-col justify-center px-20 gap-10 ">
            <div class="mt-40">
                <h1 class="text-white text-6xl">Tursted by those who <br> need a good product</h1>
                <button
                    class="px-5 py-2 bg-white w-fit rounded-full font-semibold hover:bg-black hover:text-white duration-500 delay-110 cursor-pointer hover:scale-103 mt-10">Explore
                    product ></button>
            </div>
            <div class="">
                <p class="text-[15px] text-gray-400 mb-20">Shopping online makes it easy to find exactly what you need
                    without
                    leaving home. You can compare <br>
                    prices, read reviews, and discover new products in just a few clicks. The best part is having <br>
                    everything delivered right to your doorstep.</p>
                <div class="">
                    <div class="w-70 h-40 bg-white rounded-xl  relative">
                        <div class="w-full h-full absolute bg-black/20"></div>
                        <video src="../assets/mini.mp4" autoplay muted loop class="w-full rounded-xl"></video>
                    </div>
                </div>
            </div>
        </div>
        <div class="relative">
            <div class="w-full h-[849px] bg-black/60 absolute"></div>
            <video src="../assets/background.mp4" autoplay muted loop class="w-full"></video>
        </div>
    </section>

    <!-- feautured -->
    <section class="w-full h-fit py-10 flex flex-col justify-center items-center gap-10 ">
        <h1 class="text-6xl font-semibold py-2 border-b-2 px-10 w-fit">Featured</h1>
        <div class="flex gap-5">

            <div class="max-w-sm w-full bg-black rounded-lg shadow-lg overflow-hidden ">
                <div>
                    <img class="object-cover h-64 w-full"
                        src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w0NzEyNjZ8MHwxfHNlYXJjaHw1fHxzbmVha2Vyc3xlbnwwfDB8fHwxNzEyMjIzNDAyfDA&ixlib=rb-4.0.3&q=80&w=1080"
                        alt="Converse sneakers" />
                </div>

                <div class="flex flex-col gap-1 mt-4 px-4">
                    <span class="font-normal text-gray-600 dark:text-gray-300">Accessories</span>
                    <h2 class="text-lg font-semibold text-gray-800 dark:text-gray-50">Converse Sneakers</h2>
                    <span class="font-semibold text-gray-800 dark:text-gray-50">$60</span>
                </div>

                <div class="mt-4 p-4 border-t flex justify-between border-gray-200 dark:border-gray-500">
                   <button class="rounded-full font-semibold px-5 py-2 bg-white hover:bg-black hover:text-white hover:border hover:border-white duration-500 delay-110">Add to cart</button>
                   <button class="text-white px-5 py-2 font-semibold hover:bg-white hover:text-black rounded-full duration-500 delay-110 cursor-pointer">Details</button>
                </div>
            </div>

            <div class="max-w-sm w-full bg-black rounded-lg shadow-lg  overflow-hidden ">
                <div>
                    <img class="object-cover h-64 w-full"
                        src="https://www.kimstore.com/cdn/shop/files/jbl-tune-buds-2-black_97eaa7d8-5ccd-4c3b-ada0-d59d1b492ce2.png?v=1759483551&width=980"
                        alt="Converse sneakers" />
                </div>

                <div class="flex flex-col gap-1 mt-4 px-4">
                    <span class="font-normal text-gray-600 dark:text-gray-300">Electronics</span>
                    <h2 class="text-lg font-semibold text-gray-800 dark:text-gray-50">JBL Tune Buds 2</h2>
                    <span class="font-semibold text-gray-800 dark:text-gray-50">$5,489</span>
                </div>

                <div class="mt-4 p-4 border-t flex justify-between border-gray-200 dark:border-gray-500">
                   <button class="rounded-full font-semibold px-5 py-2 bg-white hover:bg-black hover:text-white hover:border hover:border-white duration-500 delay-110">Add to cart</button>
                   <button class="text-white px-5 py-2 font-semibold hover:bg-white hover:text-black rounded-full duration-500 delay-110 cursor-pointer">Details</button>
                </div>
            </div>

            <div class="max-w-sm w-full bg-black rounded-lg shadow-lg overflow-hidden ">
                <div>
                    <img class="object-cover h-64 w-full"
                        src="https://dynamic.zacdn.com/khhMqsMeT4VEuL6xmpZOYK1qKdM=/filters:quality(70):format(webp)/https://static-ph.zacdn.com/p/hm-9506-5056683-1.jpg"
                        alt="Converse sneakers" />
                </div>

                <div class="flex flex-col gap-1 mt-4 px-4">
                    <span class="font-normal text-gray-600 dark:text-gray-300">Clothes</span>
                    <h2 class="text-lg font-semibold text-gray-800 dark:text-gray-50">Oversized Fit Zip-through hoodie</h2>
                    <span class="font-semibold text-gray-800 dark:text-gray-50">$1,290</span>
                </div>

                <div class="mt-4 p-4 border-t flex justify-between border-gray-200 dark:border-gray-500">
                   <button class="rounded-full font-semibold px-5 py-2 bg-white hover:bg-black hover:text-white hover:border hover:border-white duration-500 delay-110">Add to cart</button>
                   <button class="text-white px-5 py-2 font-semibold hover:bg-white hover:text-black rounded-full duration-500 delay-110 cursor-pointer">Details</button>
                </div>
            </div>
        </div>
    </section>

</template>