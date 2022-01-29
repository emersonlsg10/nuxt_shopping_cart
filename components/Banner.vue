<template>
  <div>
    <div
      class="relative flex banner_container"
      :style="{ backgroundImage: createBackgroundString }"
    >
      <div class="max-w-12xl mx-auto lg:px-12 content_banner">
        <div class="text_banner">
          <h1 class="title">Notebooks</h1>
          <h3 class="title_subtitle">As melhores ofertas</h3>
        </div>
      </div>
    </div>
    <div class="div_selector">
      <section>
        <input v-model="color" class="button_radio" type="radio" value="0" />
        <input v-model="color" class="button_radio" type="radio" value="1" />
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BannerLayout',
  data() {
    return {
      angle: '50',
      color1: '#8E36B7',
      color2: '#D794F6',
      a: 0,
      b: 1,
    }
  },
  computed: {
    createBackgroundString() {
      return `linear-gradient(${this.angle}deg, ${this.color1}, ${this.color2})`
    },
  },
}
</script>

<style>
.banner_container {
  height: 300px;
  background-color: #933ebd;
}

.content_banner {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex: 1;
  max-width: 85%;
}

.text_banner {
  width: 270px;
  height: 75px;
}

.title {
  color: #fff;
  font-size: 40px;
  font-weight: bold;
}

.title_subtitle {
  color: #fff;
  font-size: 20px;
  font-weight: bold;
}

.div_selector {
  justify-content: center;
  display: flex;
}

.button_radio {
  margin-right: 5px;
}
</style>
