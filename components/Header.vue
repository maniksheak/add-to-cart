<template>
    <v-app-bar>
        <v-toolbar-title @click="$router.push('/')">
            Shopping Cart Website
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn class="mx-4 text-none" @click="goCart">
            <v-badge :content="1" color="error">
                <v-icon>mdi-cart-outline</v-icon>
            </v-badge>
        </v-btn>
        <v-btn :prepend-icon="'mdi-weather-sunny'">
            <v-icon class="px-2">mdi-weather-sunny</v-icon>
            Toogle Theme
        </v-btn>
    </v-app-bar>
</template>

<script >

export default {
    methods: {
        goCart() {
            this.$router.push('/cart')
            // console.log('ddd');
        }
    }
}
</script>

<style  scoped></style>