<script>
export default {

    data() {
        return {
            userName: '',
            gmail: '',
            shippingAdd: '',
            billAdd: '',
        }
    },
    methods: {
        closeCheckOut(closemodal) {
            this.$emit('closeCheckOut', closemodal)
        },

        checkoutmodal(i){
            this.$emit('toconfirm', true);
            this.$emit('ShowCartModal', false)
            this.$emit('name', this.userName);
            this.$emit('gmail', this.gmail);
            this.$emit('addS', this.shippingAdd);
            this.$emit('addB', this.billAdd);
            this.$emit('closeCheckModal', i);
        },

        closemodal(i){
            this.$emit('closeModal', false)
        }
    }
}
</script>

<template>
    <div class="w-full flex justify-center fixed z-999 top-0 items-center bg-black/70 h-screen">
        <div class="max-w-md mx-auto bg-white rounded-lg overflow-hidden md:max-w-xl">
            <div class="md:flex">
                <div class="w-full px-6 py-8 md:p-8">
                    <h2 class="text-2xl font-bold text-gray-800">Checkout</h2>
                    <p class="mt-4 text-gray-600">Please fill out the form below to complete your purchase.</p>
                    <form class="mt-6">
                        <div class="mb-6">
                            <label class="block text-gray-800 font-bold mb-2" for="name">
                                Name
                            </label>
                            <input v-model="userName"
                                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                 type="text" placeholder="Enter Name">
                        </div>
                        <div class="mb-6">
                            <label class="block text-gray-800 font-bold mb-2" for="email">
                                Email
                            </label>
                            <input v-model="gmail"
                                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                 type="text" placeholder="sample@example.com">
                        </div>
                        

                        <div class="mb-6">
                            <label class="block text-gray-800 font-bold mb-2" for="cvv">
                                Shipping Address
                            </label>
                            <input v-model="shippingAdd"
                                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                 type="text" placeholder="Enter Address">
                        </div>
                        <div class="mb-6">
                            <label class="block text-gray-800 font-bold mb-2" for="cvv">
                                Billing Address
                            </label>
                            <input v-model="billAdd"
                                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                                 type="text" placeholder="Enter Address">
                        </div>
                        <div class="space-x-5">

                            <button @click="checkoutmodal(false)"
                                class="bg-indigo-500 hover:bg-indigo-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                               >
                                Confirm
                            </button>
                            <button @click="closemodal(false)"
                                class="bg-indigo-500 hover:bg-indigo-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                                >
                                Cancel
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>