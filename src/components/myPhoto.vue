<template>
  <div>
    <div class="all-photo">
      <h3 class="all-photo__title">Фотографии пакета:</h3>
      <div class="all-photo__block" >
        <img class="all-photo__block-item" v-for="item in items1" :key="item" :src="item.src">
        <template v-if="isShow">
              <img class="all-photo__block-item" v-for="item in items2" :key="item" :src="item.src">
        </template>
      </div>
      <div class="all-photo__button-wrap">
        <img src="./img/all-photo__button-symbol.svg" v-bind:class="rotateFun">
        <button @click="changeShow" class="all-photo__button">{{ textFun }}</button>
        <img src="./img/all-photo__button-symbol.svg" v-bind:class="rotateFun">
      </div>
      <hr class="line">
    </div>
  </div>
</template>

<script>
export default {
  name: 'myPhoto',
  data() {
    return {
      show: true,
      rotate: false,
      isShow: false,
      text: true,
      items1: [
        {src: require('./img/all-photo-block-1.jpg')},
        {src: require('./img/all-photo-block-2.jpg')},
        {src: require('./img/all-photo-block-3.jpg')},
        {src: require('./img/all-photo-block-4.jpg')},
        {src: require('./img/all-photo-block-1.jpg')},
        {src: require('./img/all-photo-block-2.jpg')},
        {src: require('./img/all-photo-block-3.jpg')},
        {src: require('./img/all-photo-block-4.jpg')},
      ],
      items2: [
        {src: require('./img/all-photo-block-4.jpg')},
        {src: require('./img/all-photo-block-3.jpg')},
        {src: require('./img/all-photo-block-2.jpg')},
        {src: require('./img/all-photo-block-1.jpg')},
        {src: require('./img/all-photo-block-4.jpg')},
        {src: require('./img/all-photo-block-3.jpg')},
        {src: require('./img/all-photo-block-2.jpg')},
        {src: require('./img/all-photo-block-1.jpg')},
      ]
    }
  },
  computed: {
    textFun() {
      return this.text ? 'Показать все фото' : 'Скрыть все фото'
    },
    rotateFun() {
      return this.rotate ? 'all-photo__button-symbol' : ''
    }
  },
  methods: {
    changeShow() {
      this.isShow = !this.isShow
      this.text = !this.text
      this.rotate = !this.rotate
      this.show = !this.show
    }
  }
}
</script>

<style scoped lang="scss">
.all-photo {
  &__title {
    font-family: Montserrat-Regular;
    font-size: 20px;
    color: #37373F;
    margin-bottom: 37px;
  }

  &__block {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-bottom: 45px;

    &_mr {
      margin-bottom: 0;
    }
  }

  &__block-item {
    margin-bottom: 10px;
  }

  &__button {
    font-family: Montserrat-Regular;
    font-size: 17px;
    border: none;
    background-color: #FFFFFF;
    color: #5286EC;
    cursor: pointer;
    margin-bottom: 27px;
    margin-right: 10px;
    margin-left: 10px;
    padding: 0;
  }

  &__button-symbol {
    transform: rotate(180deg)
  }

  &__button-wrap {
    text-align: center;
  }
}

.line {
  margin: 0;
  height: 0.5px;
  color: #C7C7C7;
  margin-bottom: 37px;
}
</style>
