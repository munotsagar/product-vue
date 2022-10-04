<template>
  <div>{{ pageTitle }}</div>
  <div><ProductList @selected="selected" /></div>
  <div><ProductDetail :product="product" /></div>
</template>

<script>
import ProductList from "./ProductList.vue";
import ProductDetail from "./ProductDetail.vue";
export default {
  name: "ManageProduct",
  components: {
    ProductList: ProductList,
    ProductDetail: ProductDetail,
  },
  data() {
    return { pageTitle: "Manage Product", product: {} };
  },
  methods: {
    selected(product) {
      this.product = product;
    },
  },
};
</script>