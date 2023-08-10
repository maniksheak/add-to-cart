<template>
    <div class="d-flex cart-outer-div">
       <div class="cart-body">
           <div v-if="totalPrice !==0" class="container mb-5">
              <h4 class="my-4 my-cart">My Cart</h4>
              <div class="d-flex my-3" style="justify-content:space-between">
                  <h4 class="fw-600">Summary</h4>
                  <h4 class="fw-600" style="margin-right: 52%"> Cart</h4>
            </div>
             <div class="d-flex">
                 <Summary></Summary>
             </div>
             <v-spacer></v-spacer>
 
              <div class="row" style="width: 50%">
                  <div style="max-width: 70%" class="col-md-12">
                    <ul style="padding: 0">
                      <li v-for="items in cartItems" :key="items" style="list-style: none">
                          <div class="cart-items">
                              <img :src="items.image" width="50px" height="50px" style="border-radius: 50%;">
                              <h6 class="mt-15"> {{ items.title }}</h6>
                              <div class="d-flex mt-10">
                                 <button  class="add" type="button">-</button>
                                 <span class="cart-quantity"> {{ items.quantity }}</span>
                                 <button  class="remove" type="button">+</button>
                              </div>
                              <h6 class="mt-15"> {{ items.price }}</h6>
                      
                            </div>
                          <div class="line"></div>
                      </li>
                    </ul>
                </div>
              </div>
              <div class="d-flex justify-content-end" style="width: 80%; margin-top: 2%">
                <v-btn  color="primary" type="button">Checkout</v-btn>
            </div>
           </div>
           <EmptyCart v-else></EmptyCart>
       </div>
       <!-- <items></items> -->
    </div>
</template>

<script>
// import Header from '../components/Header.vue'
import items from '../components/items.vue'
import Summary from '../components/Summary.vue'
import EmptyCart from '../components/EmptyCart.vue'
import data from '../store/data'
  
export default {
        name: 'Cart',

       components: {
        data,
        items,
        Summary,
        EmptyCart
       },
       methods: {
            addItem(items) {

            },
            removeItem(items) {
                
            }
       },
       computed: {
        cartItems() {
            return this.$store.data.cartItems;
        },
        // totalPrice() {
        //     let price =0;
        //     this.$store.data.cartItems.map(el => {
        //         price += el["quantity"] * el ["price"]
        //     });
        //     return price;
        // }
       }

      }
</script>

<style scoped>
   .cart-outer-div {
    flex-direction: column;
    height: 100vh;
   }
   .cart-body {
     background: white;
     flex: 1;
     overflow: auto;
   }
   .cart-quantity {
     display: inline-block;
     padding: 3px 6px;
     width: 46px;
     height: 28px;
     border-radius: 2px;
     background: white;
     margin: 0 5px;
     text-align: center;
   }
   .cart-items {
    display: flex;
    justify-content: space-between;
    padding: 10px;
    background: white;
   }
   .my-cart {
    font-size: 25px;
    color: orange;
    font-weight: 800;
   }
   input[type="text"] {
     border: none;
     width: 100%;
     font-size: 14px;
     font-weight: 500;
     vertical-align: middle;
     text-align: center;
     outline: none;
   }
   .fw-600 {
    font-size: 22px;
    font-weight: 700;
   }
   .line {
     height: 1px;
     border-bottom: 1px solid black;
   }
   .w-120 {
    width: 120%;
   }
   .w-60 {
    width: 60%;
   }
   .add, .remove {
    width: 28px;
    height: 28px;
    background: linear-gradient(#fff, #f9f9f9);
    border: 1px solid #c2c2c2;
    cursor: pointer;
    font-size: 16px;
    border-radius: 7px;
    padding-top: 1px;
    outline: none;
   }
   .mt-10 {
    margin-top: 10px;
   }
   .mt-15 {
    margin-top: 15px;
   }
   .orange-red {
    color: orangered;
   }
   .darkblue {
    color: darkblue;
   }
</style>