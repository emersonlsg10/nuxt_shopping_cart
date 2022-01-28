<template>
  <div
    class="
      relative
      flex
      items-top
      justify-center
      bg-gray-100
      sm:items-center sm:pt-0
    "
  >
    <div class="max-w-6xl">
      <div class="relative flex items-top justify-center flex-wrap mt-10">
        <Product
          v-for="product in products"
          :key="product.id"
          :product="product"
        ></Product>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductsHall',
  data() {
    return {
      products: [],
    }
  },
  async created() {
    // GET request using fetch with async/await
    const response = await fetch(
      'https://raw.githubusercontent.com/owInteractive/desafio-frontend-2020/master/produtos.json'
    )
    const data = await response.json()
    this.products = data
  },
}
</script>
