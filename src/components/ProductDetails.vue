<template>
    <div>
      <ProductItem v-for="product in products" :key="product.id" :product="product"/>
    </div>
</template>

<script>
import ProductItem from './ProductItem.vue';

export default {
    name: 'ProductDetails',
    components:{
        ProductItem
    },

    data() {
        return {
            products: [
                {
                    id: 0,
                    name: 'Полотенце',
                    price: 1000,
                    avaliable: false,
                },
                {
                    id: 1,
                    name: 'Мыло',
                    price: 1500,
                    avaliable: true,
                },
                {
                    id: 2,
                    name: 'Наволочка',
                    price: 2000,
                    avaliable: true,
                },
                {
                    id: 3,
                    name: 'Одеяло',
                    price: 2500,
                    avaliable: true,
                },

            ]

        };
    },

    methods: {

    },
};
</script>

<style lang="scss" scoped></style>