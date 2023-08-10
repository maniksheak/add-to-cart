<template>
    <div class="container my-5" style="text-align: center">
        <img src="../assets/image/shoping-cart.jpg" width="200px">
        <div class="mt-4">
            <h4 class="orange-red fw-600"> Your Cart is Empty</h4>
            <h5 class="darkblue fw-600"> You can go to home page to view more product items.</h5>
        </div>
    </div>
</template>

<script>
export default {
    name: "EmptyCart"
   }
</script>

<style scoped>
   .orange-red {
    color: red;
   }

   .darkblue{
     color: darkblue;
   }

   .fw-600 {
    font-weight: 600px;
   }
</style>