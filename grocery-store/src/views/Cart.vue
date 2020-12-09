<template>
<div>
  <div class="wrapper">
  </div>
  <h1 v-if="this.$root.$data.cart.length == 0">Cart is empty</h1>
  <CartList :products="products" />
</div>
</template>

<script>
import CartList from "../components/CartList.vue"
export default {
  name: 'Home',
  components: {
    CartList
  },
  computed: {
  products() {
    return this.$root.$data.cart;

  }
  },
}
</script>


<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
