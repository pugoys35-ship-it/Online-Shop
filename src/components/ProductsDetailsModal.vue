<script>
export default {
    props: ['mydetails'],
    data() {
        return {

        }
    },
    methods: {
        cancelModal(){
            this.mydetails.splice(0,1);
            this.$emit('detailModal', false);
        },
         addtoCart() {
            this.$emit('toCart', this.mydetails);
        },
    }
}
</script>

<template>
    <div class="bg-black/40 backdrop-blur py-8 fixed w-full h-screen top-0 z-9999   ">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div v-for="(item, index) in mydetails" class="">
                <div class="flex flex-col md:flex-row -mx-4 mt-20 ml-20">
                    <div class="md:flex-1 px-4">
                        <div class="h-[460px] rounded-lg bg-gray-300 dark:bg-gray-700 mb-4">
                            <img class="w-full h-full object-cover"
                                :src="item.image"
                                alt="Product Image">
                        </div>
                        <div class="flex -mx-2 mb-4">
                           
                            <div class="w-1/2 px-2">
                                <button @click="cancelModal"
                                    class="w-full bg-gray-200 dark:bg-gray-700 text-white dark:text-white py-2 px-4 rounded-full font-bold hover:bg-gray-300 dark:hover:bg-gray-600">Back to Products</button>
                            </div>
                        </div>
                    </div>
                    <div class="md:flex-1 px-4">
                        <h2 class="text-2xl font-bold text-white dark:text-white mb-2">{{ item.name }}</h2>
                        <p class="text-white dark:text-white text-sm mb-4">
                         {{ item.description }}
                        </p>
                        <div class="flex mb-4">
                            <div class="mr-4">
                                <span class="font-bold text-white dark:text-white">Price:</span>
                                <span class="text-white dark:text-white">$29.99</span>
                            </div>
                            <div>
                                <span class="font-bold text-white dark:text-white">Availability:</span>
                                <span class="text-gray-600 dark:text-white">In Stock</span>
                            </div>
                        </div>
                        <div class="mb-4">
                            <span class="font-bold text-white dark:text-gray-300">Color:</span>
                            <div class="flex items-center mt-2">
                                <button class="w-6 h-6 rounded-full bg-gray-800 dark:bg-gray-200 mr-2"></button>
                                <button class="w-6 h-6 rounded-full bg-red-500 dark:bg-red-700 mr-2"></button>
                                <button class="w-6 h-6 rounded-full bg-blue-500 dark:bg-blue-700 mr-2"></button>
                                <button class="w-6 h-6 rounded-full bg-yellow-500 dark:bg-yellow-700 mr-2"></button>
                            </div>
                        </div>
                        <div class="mb-4">
                            <span class="font-bold text-white dark:text-white">Size:</span>
                            <div class="flex items-center mt-2">
                                <button
                                    class="bg-gray-300 dark:bg-gray-700 text-white dark:text-white py-2 px-4 rounded-full font-bold mr-2 hover:bg-gray-400 dark:hover:bg-gray-600">S</button>
                                <button
                                    class="bg-gray-300 dark:bg-gray-700 text-white dark:text-white py-2 px-4 rounded-full font-bold mr-2 hover:bg-gray-400 dark:hover:bg-gray-600">M</button>
                                <button
                                    class="bg-gray-300 dark:bg-gray-700 text-white dark:text-white py-2 px-4 rounded-full font-bold mr-2 hover:bg-gray-400 dark:hover:bg-gray-600">L</button>
                                <button
                                    class="bg-gray-300 dark:bg-gray-700 text-white dark:text-white py-2 px-4 rounded-full font-bold mr-2 hover:bg-gray-400 dark:hover:bg-gray-600">XL</button>
                                <button
                                    class="bg-gray-300 dark:bg-gray-700 text-white dark:text-white py-2 px-4 rounded-full font-bold mr-2 hover:bg-gray-400 dark:hover:bg-gray-600">XXL</button>
                            </div>
                        </div>
                        <div>
                            <span class="font-bold text-white dark:text-white">Product Description:</span>
                            <p class="text-white dark:text-white text-sm mt-2">
                              {{ item.description }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>