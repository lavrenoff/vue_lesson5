<template>
    <article class="prd">
       <h2>Наименование товара: {{ product.name }}</h2> 
       <p>Цена в рублях: {{ product.price }}</p>       
       <p>Цена в долларах: {{ formattedPrice(product.price) }}</p>
       <p v-if="product.avaliable" style="color: green;">avaliable</p>
       <p v-else style="color: red;">Out of stock</p>
    </article>
</template>

<script>
export default {
    name: 'ProductItem',
    props:['product'],

    data() {
        return {
            
        };
    },    

    methods: {
        formattedPrice(price){
            return new Intl.NumberFormat("ru", {style: "currency", currency: "USD"}).format(price/100);
        }
    },
};
</script>

<style scoped>
.prd {
 border:1px solid black;
 margin: 10px;
 border-radius: 10px;
 width: 500px;
}

</style>