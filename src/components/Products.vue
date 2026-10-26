<script>
export default {
    props: ['toproducts'],
    data() {
        return {

        }
    },
    methods: {
        addtoCart(index) {
            this.$emit('toCart', index);
        },

        addtoDetails(index){
            this.$emit('details' , this.toproducts[index]);
            this.$emit('modalD' , true);
        }
    }
}
</script>

<template>
    <div class="w-full h-fit py-20 flex flex-col items-center">
        <div class="w-330 rounded-[20px] h-fit bg-linear-to-b from-black via-black/90 to-black/80 p-5 ">
            <div class="flex items-center w-full">
                <input type="text" placeholder="Search" class="px-5 py-2 w-full  bg-white rounded-l-lg ">
                <button class="px-10 py-2 bg-gray-300 rounded-r-lg font-semibold">Search</button>
            </div>
            <div class="w-full flex justify-between mt-5">
                <div class=" space-x-5  ">
                    <button class="bg-white px-5 py-2 rounded-full font-semibold cursor-pointer">Electronics</button>
                    <button class="bg-white px-5 py-2 rounded-full font-semibold cursor-pointer">Clothes</button>
                    <button class="bg-white px-5 py-2 rounded-full font-semibold cursor-pointer">Accessories</button>
                </div>
                <select name="" id="" class="w-60 outline-none cursor-pointer bg-white px-5 py-2 rounded-xl font-semibold fucos:border-white">
                    <option value="">Highest to Lowest Price</option>
                    <option value="">Lowest to Highest Price</option>
                </select>
            </div>
        </div>

        <div class="grid grid-cols-4 gap-5 mt-10">
            <div v-for="(item, index) in toproducts" :key="index.id">
                <div class="max-w-sm w-full bg-black rounded-lg shadow-lg overflow-hidden ">
                    <div>
                        <img class="object-cover h-54 w-full" :src="item.image" alt="Converse sneakers" />
                    </div>

                    <div class="flex flex-col gap-1 mt-4 px-4">
                        <span class="font-normal text-gray-600 dark:text-gray-300">{{ item.category }}</span>
                        <h2 class="text-md font-semibold text-gray-800 dark:text-gray-50">{{ item.name }}</h2>
                        <span class="font-semibold text-gray-800 dark:text-gray-50">${{ item.price }}</span>
                    </div>

                    <div class="mt-4 p-4 border-t flex justify-between border-gray-200 dark:border-gray-500">
                        <button @click="addtoCart(index)"
                            class="rounded-full font-semibold px-5 py-2 bg-white hover:bg-black hover:text-white hover:border hover:border-white duration-500 delay-110">Add
                            to cart</button>
                        <button @click="addtoDetails(index)"
                            class="text-white px-5 py-2 font-semibold hover:bg-white hover:text-black rounded-full duration-500 delay-110 cursor-pointer">Details</button>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>