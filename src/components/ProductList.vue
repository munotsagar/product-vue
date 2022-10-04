<template>
  <div>{{ pageTitle }}</div>
  <div>
    <table>
      <tr>
        <th>Id</th>
        <th>Name</th>
        <th>Price</th>
      </tr>
      <tr v-for="product in products" :key="product.id">
        <td>
          {{ product.id }}
        </td>
        <td>
          <a @click="showProductDetails(product.id)"> {{ product.name }}</a>
        </td>
        <td>
          {{ product.price }}
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "ProductList",
  data() {
    return {
      pageTitle: "Product List",
      products: [
        {
          id: 1,
          name: "Product 1",
          price: "$100",
        },
        {
          id: 2,
          name: "Product 2",
          price: "$200",
        },
        {
          id: 3,
          name: "Product 3",
          price: "$300",
        },
      ],
    };
  },
  methods: {
    showProductDetails(id) {
      let product = this.products.filter((product) => product.id == id);
      this.$emit("selected", product[0]);
      //return product[0];
    },
  },
};
</script>