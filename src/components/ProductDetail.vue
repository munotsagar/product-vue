<template>
  <div>{{ pageTitle }}</div>
  <div v-if="product">
    <form>
      <table>
        <td>Product Id: {{ product.id }}</td>
        <td>
          Product Name:
          <input type="text" v-model="productname.name" />
        </td>
        <td>Product Price: {{ product.price }}</td>
      </table>
    </form>
  </div>
</template>

<script>
export default {
  name: "ProductDetail",
  props: ["product"],
  data() {
    return {
      pageTitle: "Product Detail",
      productname: this.product,
    };
  },
};
</script>