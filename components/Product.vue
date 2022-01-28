<template>
  <div class="card_product">
    <div class="image_container">
      <img :src="product.imageUrl" class="product_image" alt="Product Name" />
    </div>
    <div class="product_container">
      <div class="product_info">
        <p class="product_category">{{ product.category }}</p>
        <p class="product_name">{{ product.name }}</p>
        <div class="product_description">
          {{ product.description }}
        </div>
        <p class="product_price">{{ formatPrice(product.price) }}</p>
      </div>
      <hr class="divider" />
      <div class="container_button">
        <button class="button" type="button">ADICIONAR AO CARRINHO</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductComponent',
  // eslint-disable-next-line vue/require-prop-types
  props: ['product'],
  methods: {
    formatPrice(value) {
      return parseFloat(value).toLocaleString('pt-BR', {
        minimumFractionDigits: 2,
        maximumFractionDigits: 2,
        style: 'currency',
        currency: 'BRL',
      })
    },
  },
}
</script>

<style>
.card_product {
  width: 300px;
  height: 410px;
  box-shadow: 1px 1px 3px 1px #888888;
  margin-right: 20px;
  margin-bottom: 20px;
}

.image_container {
  height: 45%;
}

.product_image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.product_container {
  height: 55%;
}

.product_info {
  padding-top: 15px;
  padding-left: 20px;
  padding-right: 50px;
}

.product_category {
  color: #933ebd;
  font-weight: 500;
  font-size: 12px;
}

.product_name {
  font-weight: 500;
  font-size: 15px;
  margin-top: 5px;
  height: 20px;
  overflow: hidden;
  text-overflow: ellipsis;
}

.product_description {
  font-weight: 400;
  font-size: 13px;
  margin-top: 5px;
  height: 40px;
  overflow: hidden;
  text-overflow: ellipsis;
}

.product_price {
  font-weight: 600;
  font-size: 20px;
  margin-top: 15px;
}

.divider {
  margin-top: 20px;
  border-color: #a6a6a6;
  border-width: 1px;
}

.container_button {
  overflow: hidden;
}

.button {
  color: #933ebd;
  background-color: #fff;
  width: 100%;
  height: 56px;
  font-size: 14px;
  font-weight: 600;
}

.button:hover {
  background-color: #933ebd;
  color: #fff;
  width: 100%;
  height: 56px;
  font-size: 14px;
  font-weight: 600;
}
</style>
