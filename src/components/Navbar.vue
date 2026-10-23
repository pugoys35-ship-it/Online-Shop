<script>
export default {
    props:['page'],
    data() {
        return {

        }
    },
    methods: {
        navi(page) {
            this.$emit('goTo', page);
        },

        showCartModal(modal) {
            this.$emit('showModalCart', modal);
        }
    }
}
</script>

<template>


    <nav v-if="page === 'Home'" class="flex  justify-between px-15 items-center absolute w-full z-999 ">
        <div class="flex items-center gap-10">
            <img src="../assets/logo.png" alt="" class="h-30 w-30 object-cover">
            <p @click="navi('Home')" class="text-gray-400 font-semibold text-md cursor-pointer  ">Home</p>
            <p @click="navi('Products')" class="text-gray-400 font-semibold text-md cursor-pointer">Products</p>

        </div>
        <div class="z-999">
            <button @click="showCartModal(true)"
                class="px-5 py-2 bg-white rounded-xl text-black hover:bg-black hover:text-white duration-500 delay-110 hover:scale-103 cursor-pointer ">Cart</button>
        </div>
    </nav>

    <nav v-if="page === 'Products'" class="flex  justify-between px-15 items-center w-full z-999 ">
        <div class="flex items-center gap-10">
            <img src="../assets/productLogo.png" alt="" class="h-30 w-30 object-cover">
            <p @click="navi('Home')" class="text-black font-semibold text-md cursor-pointer  ">Home</p>
            <p @click="navi('Products')" class="text-black font-semibold text-md cursor-pointer">Products</p>

        </div>
        <div class="z-999">
            <button @click="showCartModal(true)"
                class="px-5 py-2 bg-black rounded-xl text-white hover:border hover:bg-white hover:border-blacks hover:text-black duration-500 delay-110 hover:scale-103 cursor-pointer ">Cart</button>
        </div>
    </nav>


</template>