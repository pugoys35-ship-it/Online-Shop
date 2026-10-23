<script>
export default{
    data(){
        return{

        }
    },
    methods: {
        CloseModal(closemodal){
            this.$emit('ShowCartModal', closemodal);
        },

        showCheckOutModal(modal){
            this.$emit('showCheckModal', modal)
        }
    }
}
</script>

<template>
    <div class="w-full h-fit flex justify-end px-10 fixed right-0 z-999 top-50">
        <div class="w-80">
            <div class="bg-white rounded-lg shadow-md p-6">
                <div class="flex justify-between items-center mb-4">
                    <h2 class="text-lg font-semibold ">Summary</h2>
                    <button @click="CloseModal(false)" class="text-xl cursor-pointer">↳</button>
                </div>
                <hr class="my-2">



                <hr class="my-2">
                <div class="flex justify-between mb-2">
                    <span>Subtotal</span>
                    <span>$19.99</span>
                </div>
                <div class="flex justify-between mb-2">
                    <span>Shipping</span>
                    <span>$0.00</span>
                </div>
                <hr class="my-2">
                <div class="flex justify-between mb-2">
                    <span class="font-semibold">Total</span>
                    <span class="font-semibold">$21.98</span>
                </div>
                <button @click="showCheckOutModal(true)"
                    class="bg-black text-white hover:border hover:bg-white hover:border-black hover:text-black cursor-pointer duration-400 delay-110 py-2 px-4 rounded-lg mt-4 w-full">Checkout</button>
            </div>
        </div>
    </div>
</template>