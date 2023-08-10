<template>
    <div>
        <v-row class="my-5">
            <v-col cols="12">
                <v-btn color="bg-primary">
                    <v-icon>mdi-view-list</v-icon>
                </v-btn>
                <v-btn class="bg-primary">
                    <v-icon>mdi-apps</v-icon>
                </v-btn>
            </v-col>
        </v-row>

        <v-row>
            <v-col cols="12">
                <v-row>
                    <v-col v-for="(product, i) in products" :key="i" cols="12" lg="3" sm="6">
                        <v-card class="mx-auto pb-3">
                            <v-img :src="product.image" height="300px" cover>
                                <template v-slot:placeholder>
                                    <v-row align="center" class="fill-height  ma-0" justify="center">
                                        <v-progress-circular color="gray lighten-5" indeterminate> </v-progress-circular>
                                    </v-row>
                                </template>
                            </v-img>
                            <v-card-title class="text-capitalize">
                                {{ product.title }}
                            </v-card-title>

                            <v-card-subtitle class="pt-2">
                                {{ product.price }}
                            </v-card-subtitle>

                            <v-card-actions>
                                <v-btn color="bg-primary"> Read More</v-btn>
                                <v-spacer></v-spacer>
                                <!-- <v-btn class="bg-primary" @click="cartStore.add(product.id)">
                                Add to Cart
                             </v-btn> -->
                                <v-btn class="primary">
                                    Add to Cart
                                </v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </div>
</template>
  
<script>
import items from '../store/data';
// import axios from 'axios'


// const grid = ref(data)

export default {

    data() {
        return {
            products: items
        }
    },
    mounted() {
        // this.loadData()
    },
    methods: {
        //     async loadData() {
        //         try {
        //             const data = await axios.get("https://api.escuelajs.co/api/v1/products"
        //   );

        //   this.products = data.data;
        //    console.log(data.data);
        //         } catch (error) {

        //         }

        // }

    },

}
</script>
  
<style lang="scss" scoped></style>

