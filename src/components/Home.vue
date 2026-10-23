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
                <p class="text-[15px] text-gray-400 mb-20">Shopping online makes it easy to find exactly what you need without
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
    

</template>