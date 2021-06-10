<template>
    <div class="container">
        <div class="container-navbar">
            <a class="navbar-brand text-dark" href="#">Shopping Cart</a>
            <a class="navbar-brand text-dark cart" href="#">
                Cart ({{ totalQty }})
            </a>
        </div>
    </div>
</template>
<script>
import { mapGetters } from 'vuex'
export default {
    name: "Header",
    computed: {
        ...mapGetters(["cart"]),
        totalQty() {
            return this.cart.reduce((a,b) =>a + b.qty, 0);
        }
    }
}
</script>

<style scoped>
    .cart {
        float: right;
    }
    .container-navbar {
        margin-bottom: 50px;
    }
</style>