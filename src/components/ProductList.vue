<template>
    <div class="row">
        <div class="card mb-5" style="width: 15rem;" v-for="item in products" :key="item.id">
            <img 
                class="card-img-top" 
                :src="item.imgFile" 
                alt="Card image cap"
            >
            <div class="card-body">
                <p class="card-title">{{ item.title }}</p>
                <p class="card-text text-success">
                    $ {{ item.price }}
                </p>
                <a href="#" @click="addToCart(item)" class="btn btn-primary">Add to cart</a>
            </div>
        </div>
    </div>
</template>
<script>
import { mapGetters, mapActions } from 'vuex'
// import products from '../mock/products.json'
export default {
    name: "ProductList",
    computed: {
        ...mapGetters(["products"])
    },
    methods: {
        ...mapActions(["getProducts", "addToCart"])
    },
    mounted() {
        this.getProducts()
    }
    // data() {
    //     return {
    //         products,
    //     }
    // },

    // computed: {
    //     ...mapGetters(["products"])
    // },
    // methods: {
    //     ...mapActions((["getProducts"]))
    // },
    // mounted() {
    //     this.getProducts();
    // }

}
</script>

<style scoped>
    .card {
        border: 1px solid #eaeaea;
        box-shadow: 0px 0px 5px rgba(49, 49, 49, 0.5);
        border-radius: 10px;
        margin-left: 5px;
    }
    .card:hover {
        transform: scale(1.02);

    }
</style>