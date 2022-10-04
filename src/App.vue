<template>
  <ManageProduct />
</template>

<script>
import ManageProduct from "./components/ManageProduct.vue";
export default {
  name: "App",
  components: {
    ManageProduct: ManageProduct,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
