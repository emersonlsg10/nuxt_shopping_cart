<template>
  <div class="relative flex header">
    <div class="max-w-5xl mx-auto sm:px-6 lg:px-8 container_center">
      <div>
        <h1 class="mkt">MKT<span class="place">Place</span></h1>
      </div>
      <div class="container_cart_header">
        <h2 class="produtos">Produtos</h2>
        <img :src="cartSvg" />
        <div class="div_counter">
          <span class="counter">5</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderLayout',
  data() {
    return {
      cartSvg: '',
    }
  },
  created() {
    this.cartSvg = require(`../resources/icons/shopping-cart.svg`)
  },
}
</script>

<style>
.header {
  height: 60px;
}

.container_center {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.mkt {
  color: #909090;
  font-size: 20px;
  font-weight: bold;
}

.place {
  color: #933ebd;
  font-size: 20px;
  font-weight: bold;
}

.produtos {
  color: #909090;
  font-size: 14px;
  font-weight: bold;
  margin-right: 5px;
}

.container_cart_header {
  display: flex;
  align-items: center;
  padding-right: 15px;
}

.div_counter {
  background-color: #ed1c24;
  border-radius: 25px;
  height: 15px;
  width: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 10px;
}

.counter {
  color: #fff;
  font-size: 10px;
  font-weight: bolder;
}
</style>