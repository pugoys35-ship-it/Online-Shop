<script>
export default {
    props: ['toCartItem', 'subT'],
    data() {
        return {
            addquan: 0,
             
        }
    },
    methods: {
        CloseModal(closemodal) {
            this.$emit('ShowCartModal', closemodal);
        },

        showCheckOutModal(modal) {
            this.$emit('showCheckModal', modal)
        },

        removeCart(index){
            this.toCartItem[index].quantity = 1;
            this.toCartItem.splice(index,1);
        },

        add(index){
            this.toCartItem[index].quantity += 1;
            this.addquan += 1;
        },

        minus(index){
            this.addquan -= 1;
            this.toCartItem[index].quantity -= 1;
        }
    }
}
</script>

<template>

    <div class="bg-white rounded-lg shadow-md p-6 fixed z-999 top-0 right-0 mr-5 mt-40 w-120">
        <div class="flex justify-between items-center mb-4">
            <h2 class="text-lg font-semibold ">Summary</h2>
            <button @click="CloseModal(false)" class="text-xl cursor-pointer">↳</button>
        </div>
        <hr class="my-2">

        <div class="w-full max-h-60 overflow-scroll ">
            <div v-for="(item, index) in toCartItem">
                <div class="flex items-center gap-3 mb-2 justify-between">
                    <div class="flex gap-3 items-center">
                        <div class="border border-black rounded-lg w-fit">
                            <img :src="item.image" alt="" class="w-20 h-20 rounded-lg">
                        </div>
                        <div>
                            <p class="text-[14px] font-semibold text-gray-500">{{ item.category }}</p>
                            <p class="text-[14px] font-semibold">{{ item.name }}</p>
                            <p class="text-[14px] font-semibold">Quantity: {{ item.quantity }}</p>
                            <p class="text-[14px] font-semibold text-emerald-500">${{ item.price }}</p>
                        </div>
                    </div>
                    <div class="flex gap-2">
                        <button @click="add(index)" class="bg-gray-200 w-8 h-8 text-lg rounded-lg border cursor-pointer">+</button>
                        <button @click="minus(index)" class="bg-gray-200 w-8 h-8 text-lg rounded-lg border cursor-pointer">-</button>
                        <button @click="removeCart(index)" class="text-[14px] bg-red-600 px-5 py-2 text-white font-semibold rounded-xl cursor-pointer hover:saturate-110">Remove</button>
                    </div>
                </div>
            </div>
        </div>

        <hr class="my-2">
        <div class="flex justify-between mb-2">
            <span>Total Items:</span>
            <span>{{ toCartItem.length }}</span>
        </div>
        <div class="flex justify-between mb-2">
            <span>Subtotal</span>
            <span>$</span>
        </div>
        <hr class="my-2">
        <div class="flex justify-between mb-2">
            <span class="font-semibold">Total</span>
            <span class="font-semibold">$21.98</span>
        </div>
        <button @click="showCheckOutModal(true)"
            class="bg-black text-white hover:border hover:bg-white hover:border-black hover:text-black cursor-pointer duration-400 delay-110 py-2 px-4 rounded-lg mt-4 w-full">Checkout</button>
    </div>

</template>