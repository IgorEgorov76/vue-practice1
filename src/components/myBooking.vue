<template>
  <div class="booking">
    <h3 class="booking__title">Доступная съемка в ближайшее время:</h3>
    <div class="booking__wrap">
      <div class="booking__data">
        <div class="booking__text"> Пятница, <b>14</b> сентября</div>
      <img src="./img/calendar.svg">
      </div>
      <div class="booking__item">
        <div class="booking__item-wrap">
          <span class="booking__item-text">15:00 - 18:00</span>
          <span class="booking__item-text"><b>1500₽</b></span>
          <span class="booking__item-text">Осталось – 1 место</span>
        </div>
        <button class="booking__item-button">Выбрать</button>
      </div>
      <div class="booking__item">
        <div class="booking__item-wrap">
          <span class="booking__item-text">19:00 - 22:00</span>
          <span class="booking__item-text"><b>1500₽</b></span>
          <span class="booking__item-text">Осталось – 1 место</span>
        </div>
        <button class="booking__item-button">Выбрать</button>
      </div>
      <div class="booking__footer">
        <img src="./img/footer-block-logo.svg">
        <span class="booking__footer-item">Более
          <span class="booking__footer-item_bold">50</span>
          отзывов с оценкой</span>
        <img src="./img/footer-block-stars.svg">
      </div>
    </div>
  </div>
</template>

<script>
export default {


}
</script>

<style scoped lang="scss">
.booking {
  margin-bottom: 100px;

  &__title {
    font-family: Montserrat-Regular;
    font-size: 20px;
    color: #37373F;
    margin-bottom: 30px;
    max-width: 250px;
   }

  &__wrap {
    max-width: 770px;
    border: 2px solid #C7C7C7;
    margin-bottom: 82px;
  }

  &__data {
    display: flex;
    padding-top: 30px;
    padding-bottom: 20px;
    padding-left: 30px;
  }

  &__text {
    font-family: Montserrat-Regular;
    font-size: 18px;
    color: #37373F;
    margin-top: auto;
    margin-bottom: auto;
    margin-right: 14px;
  }

  &__item {
    border-top: 0.5px solid #C7C7C7;
    padding: 20px 30px;
    display: flex;
    justify-content: space-between;
  }

  &__item-wrap {
    display: flex;
    flex-direction: column;
  }

  &__item-text {
    font-family: Montserrat-Regular;
    font-size: 18px;
    color: #37373F;
    margin-bottom: 10px;
  }

  &__item-text:last-child {
    margin-bottom: 0;
  }

  &__item-button {
    font-family: Montserrat-Medium;
    font-size: 14px;
    width: 129px;
    height: 50px;
    margin-top: auto;
    margin-bottom: auto;
    color: #FC9B09;
    background-color: #FFFFFF;
    border: 2px solid #FC9B09;
    cursor: pointer;
  }

  &__footer {
    max-width: 570px;
    display: flex;
    padding-left: 30px;
    padding-top: 60px;
    padding-bottom: 48px;
  }

  &__footer-item {
      margin-top: auto;
      margin-bottom: auto;
      font-family: Montserrat-Regular;
      font-size: 18px;
      margin-left: 12px;
      margin-right: 14px;

      &_bold {
        font-weight: 600;
      }
    }
}
</style>
