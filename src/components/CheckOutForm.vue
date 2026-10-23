<script>
export default{

    data(){
        return{

        }
    },
    methods:{
        closeCheckOut(closemodal){
            this.$emit('closeCheckOut', closemodal)
        }
    }
}
</script>

<template>
    <div class="w-full flex justify-center fixed z-999 top-0 items-center bg-black/70 h-screen">
        <div class="w-full max-w-md bg-white rounded-2xl shadow-lg p-6 md:p-8 h-fit">
            <!-- Header -->
            <h2 class="text-2xl font-bold text-gray-800 text-center">Checkout</h2>
            <p class="text-gray-500 text-center mt-1">Complete your purchase</p>

            <!-- Product Details -->
            <!-- <div class="mt-6 flex items-center space-x-4">
                <img src="https://media.istockphoto.com/id/913851526/photo/white-headphones.webp?a=1&b=1&s=612x612&w=0&k=20&c=1XeKlfmsO28pA3VLjiJFvvyl9AwFYjilm5AOMJGrwqM="
                    alt="Product Image" class="w-20 h-20 rounded-lg shadow">
                <div>
                    <h3 class="text-lg font-semibold text-gray-800">Wireless Headphones</h3>
                    <p class="text-sm text-gray-500">Noise Cancelling, Bluetooth 5.0</p>
                </div>
            </div> -->

            <!-- Price Breakdown -->
            <div class="mt-6 space-y-3">
                <div class="flex justify-between text-gray-600">
                    <span>Subtotal</span>
                    <span>$149.99</span>
                </div>
                <div class="flex justify-between text-gray-600">
                    <span>Shipping</span>
                    <span class="text-green-500">Free</span>
                </div>
                <div class="flex justify-between font-semibold text-gray-800">
                    <span>Total</span>
                    <span>$149.99</span>
                </div>
            </div>

            <!-- Payment Options -->
            <div class="mt-6">
                <label class="block text-gray-700 font-medium mb-2">Payment Method</label>
                <div class="flex items-center space-x-3">
                    <button class="flex-1 bg-gray-100 hover:bg-gray-200 transition p-3 rounded-lg">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/Mastercard-logo.svg"
                            alt="Mastercard" class="h-6 mx-auto">
                    </button>
                    <button class="flex-1 bg-gray-100 hover:bg-gray-200 transition p-3 rounded-lg">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/0/04/Visa.svg" alt="Visa"
                            class="h-6 mx-auto">
                    </button>
                    <button class="flex-1 bg-gray-100 hover:bg-gray-200 transition p-3 rounded-lg">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal"
                            class="h-6 mx-auto">
                    </button>
                </div>
            </div>

            <!-- Checkout Button -->
            <button 
                class="cursor-pointer mt-6 w-full bg-black hover:bg-black/90 text-white font-medium py-3 rounded-lg shadow-md hover:shadow-lg transition duration-200">
                Complete Purchase
            </button>

            <!-- Secure Payment Notice -->
              <button  @click="closeCheckOut(false)"
                class="mt-4 cursor-pointer mt-6 w-full bg-black hover:bg-black/90 text-white font-medium py-3 rounded-lg shadow-md hover:shadow-lg transition duration-200">
                Cancel Checkout
            </button>
        </div>
    </div> 
</template>