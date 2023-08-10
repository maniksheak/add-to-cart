<template>
    <div class="row" style="width: 50%">
        <div class="col-md-4">
            <h6>Total: </h6>
            <h6>Promo Code: </h6>
            <h6> Shipping: </h6>
            <div class="my-3 line w-120"></div>
            <h6>Subtotal: </h6>
        </div>
        <div class="col-md-4">
            <h6>Rs {{ totalPrice }}</h6>
            <h6>SWEETDISH</h6>
            <h6>Rs 50</h6>
            <div class="my-3-line-w-60"></div>
            <h6>Rs {{ totalPrice + 50 }}</h6>
        </div>
    </div>
</template>

<script>
export default {
    name: "Summary",
    props: ["totalPrice"]
}
</script>

<style scoped>
.line {
    padding-top: 13px;
    height: 1px;
    border-bottom: 1px solid black;
}
.col-md-4 {
    /* line-height: 1; */
    padding-bottom: 15px;
}
 h6 {
    font-size: 16px;
 }

.w-120 {
    width: 120%;
}

.w-60 {
    width: 50%;
}
</style>