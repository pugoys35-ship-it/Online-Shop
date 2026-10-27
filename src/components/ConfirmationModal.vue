<script>
export default {
    data() {
        return {

        }
    },
    methods: {

    },

    mounted(){
        setTimeout(() => {
            this.$emit('toconfirm', false)
        }, 4000)
    }
}
</script>

<template>
    <div class="fixed inset-0 z-[1000] flex items-center justify-center bg-black/50 p-4">
        <div class="relative w-full max-w-md rounded-2xl bg-white p-6 shadow-2xl">

            <div class="text-center">
                <div class="mx-auto mb-4 flex h-14 w-14 items-center justify-center rounded-full bg-blue-100">
                  <img src="../assets/check.gif" alt="" class="object-cover ">
                </div>

                <h2 class="text-xl font-bold text-gray-900">Thank You</h2>

                <p class="mt-2 text-sm text-gray-600">
                    <!-- @if (confirmationAction() === 'accept') {
              Are you sure you want to mark this  as
              <strong>Accepted</strong>?
            } -->

                    <!-- @if (confirmationAction() === 'reject') {
              Are you sure you want to mark this  as
              <strong>Rejected</strong>?
            } -->
                </p>
            </div>

            <div class="mt-6 flex gap-3">
                <p class="text-center">Thank you for your purchase. We appreciate your business and look forward to serving you again.</p>
            </div>
        </div>
    </div>
</template>