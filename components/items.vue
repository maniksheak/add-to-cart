<template>
    <div>
        <v-row class="my-5">
            <v-col cols="12">
                <v-btn @click="grid = !grid" :class="{ 'bg-primary': grid }">
                    <v-icon>mdi-view-list</v-icon>
                </v-btn>
                <v-btn @click="grid = !grid" :class="{ 'bg-primary': !grid }" class="ml-3">
                    <v-icon>mdi-apps</v-icon>
                </v-btn>
            </v-col>
        </v-row>

        <v-row>
            <v-col cols="12">
                <v-row>
                <v-col v-for="(product, i) in products" :key="i" cols="12" lg="4" sm="6">
                    <v-card class="mx-auto pb-2">
                        <v-img :src="product.image" height="200px" cover>
                            <template v-slot:placeholder>
                                <v-row align="center" class="fill-height  ma-0" justify="center"> 
                                    <v-progress-circular color="gray lighten-5" indeterminate> </v-progress-circular>
                                </v-row>
                            </template>
                        </v-img>
                        <p class="px-3 py-4"> {{ product.title }}</p>
                        <p class="px-3"> {{ product.price }}</p>

                        <v-btn class="bg-primary">Submit</v-btn>
                    </v-card>
                </v-col>
            </v-row>
            </v-col>
        </v-row>
    </div>
</template>
  
<script>
import items from '../store/data'
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

