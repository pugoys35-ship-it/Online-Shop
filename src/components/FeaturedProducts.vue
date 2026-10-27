<script>
</script>

<template>
    <div class="bg-[#141414]">

        <div class="container mx-auto px-4 py-8">
            <h2 class="text-3xl font-semibold text-center text-gray-800 dark:text-gray-200 mb-8">
                Featured Resources
            </h2>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-white dark:bg-black shadow-lg rounded-lg overflow-hidden">
                    <video src="../assets/goPro.mp4" autoplay muted loop class="w-full h-64 object-cover"></video>
                    <div class="p-4 md:p-6 border-t border-[#1B1B1B]">
                        <h3 class="text-xl font-semibold text-indigo-500 dark:text-white mb-2">Electronics</h3>
                        <p class="text-gray-700 dark:text-gray-300 mb-4 two-lines">
                            Electronics make daily tasks faster and more efficient, from communication to entertainment.
                            <br>
                            <br>
                        </p>
                        <button 
                            class="cursor-pointer inline-block bg-[#E1E1E1] font-semibold px-4 py-2 rounded-full">Learn
                            More</button>
                    </div>
                </div>

                <div class="bg-white dark:bg-black shadow-lg rounded-lg overflow-hidden">
                    <video src="../assets/clothes.mp4" autoplay muted loop class="w-full h-64 object-cover"></video>
                    <div class="p-4 md:p-6 border-t border-[#1B1B1B]">
                        <h3 class="text-xl font-semibold text-purple-500 dark:text-white mb-2">Clothes</h3>
                        <p class="text-gray-700 dark:text-gray-300 mb-4 two-lines">Clothes help you express your
                            personal style while keeping you comfortable in different weather and situations.</p>
                        <button 
                            class="cursor-pointer inline-block bg-[#E1E1E1] font-semibold px-4 py-2 rounded-full">Learn
                            More</button>
                    </div>
                </div>

                <div class="bg-white dark:bg-black shadow-lg rounded-lg overflow-hidden">
                    <video src="../assets/rolex.mp4" autoplay muted loop class="w-full h-64 object-cover"></video>
                    <div class="p-4 md:p-6 border-t border-[#1B1B1B]">
                        <h3 class="text-xl font-semibold text-cyan-500 dark:text-white mb-2">Accessories</h3>
                        <p class="text-gray-700 dark:text-gray-300 mb-4 two-lines">Accessories add personality to any
                            outfit, helping you express your style with small but meaningful details.</p>
                        <button 
                            class="cursor-pointer inline-block bg-[#E1E1E1] font-semibold px-4 py-2 rounded-full">Learn
                            More</button>
                    </div>
                </div>

                <!-- Add more items as needed, following the same structure -->

            </div>
        </div>
    </div>
</template>