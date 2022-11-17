<template>
  <div>
    <div class="container">
      <header class="header">
        <div class="logo-block">
          <img class="logo-img" src="./assets/img/HELYFLY-logo.svg">
          <div class="number-phone"><span class="number-phone_gray">Телефон:</span>8(800)-123-12-12</div>
        </div>
      </header>
      <div class="img-block">
        <div class="img-block__text">
          Эксклюзивная<span class="img-block__text_orange"> фотосессия </span>при полете на вертолете
        </div>
        <div class="img-block__price">
          <img class="price-window" src="./assets/img/price-window.svg">
          <div class="price-window-block" >
            <span class="price-window-text">Стоимость:</span>
            <br>
            <span class="price-window-price">1500₽</span>
          </div>
          <img class="symbol-percent" src="./assets/img/symbol-percent.svg">
        </div>
        <button class="price-window-buttom" type="button">Забронировать место</button>
      </div>
    </div>
    <div class="container_main">
      <div class="main-info-block">
        <div class="main-info">
          <h2 class="main-info__title">Фотосессия в вертолете</h2>
          <div class="main-info__text">Полет на вертолете это прекрасная возможность получить новые ощущения!
            А наш замечательный фотограф запечатлит лучшие моменты</div>
          <div class="main-info__item">
            <img src="./assets/img/time-logo.svg">
            <span class="main-info__item-text">3 часа сьемки</span>
          </div>
          <div class="main-info__item">
            <img src="./assets/img/camera-logo.svg">
            <span class="main-info__item-text">Более 50 фотографий</span>
          </div>
          <div class="main-info__item">
            <img src="./assets/img/place-logo.svg">
            <span class="main-info__item-text">Москва</span>
          </div>
          <div class="main-info__item">
            <img src="./assets/img/speech-bubble-logo.svg">
            <span class="main-info__item-text">Готовы ответить на любые вопросы</span>
          </div>
        </div>
        <img src="./assets/img/main-info-block-photo.jpg" class="main-info-photo">
      </div>
      <div class="text-block">
        <img src="./assets/img/text-block-logo.svg">
        <span class="text-block__item">Более
          <span class="text-block__item_bold">50</span>
          отзывов с оценкой</span>
        <img src="./assets/img/text-block-stars.svg">
      </div>
    </div>
    <div class="container_main">
      <my-photo></my-photo>
    </div>
    <div class="container_main">
      <div class="organizer-block">
        <div class="organizer-block__left">
          <div class="organizer-block__left-name">Об организаторе:</div>
          <div class="organizer-block__left-text">
            Всем привет! Я фотограф Мария!
            И по мимо фотосъемки я так же являюсь членом группы экспертов туристической отрасли,
            которые хорошо разбираются в маркетинге, операциях и услугах обслуживания клиентов,
            с пециализирующихся на совместном использовании и частных турах.
            <br><br>
            Сначала мы (я и моя команда) изучаем интересы клиентов, а затем придумываем подходящее решение,
            которое соответствует бюджету
            и планам клиента. Мы никогда не зависим от субпоставщиков и не свяжемся.
            {{ showTextFun1 }}
          </div>
          <button
              @click="changeShow1"
              class="organizer-block__left-button organizer-block__left-button_mr">
            {{ textFun1 }}
          </button>
          <img v-bind:class="rotateFun1" src="./assets/img/button-symbol.svg">
          <div class="organizer-block__left-name">Что я предоставлю:</div>
          <div class="organizer-block__left-text">
            Встречу вас на машине после длительного перелёта.
            Качественный подбор места и локации для вашей съемки.
            При необходимости всегда возможно прерваться на обед/ужин.
            Более <b>50</b> фотографий на выходе с обработкой и замечательные впечатления о Дубае !
            {{ showTextFun2 }}
          </div>
          <button
              @click="changeShow2"
              class="organizer-block__left-button">
            {{ textFun2 }}
          </button>
          <img v-bind:class="rotateFun2" src="./assets/img/button-symbol.svg">
        </div>
        <div class="organizer-block__right">
          <img class="organizer-block__right-img" src="./assets/img/organizer-block__right-img.jpg">
          <div class="organizer-block__right-name">Марина Иванова</div>
          <div class="organizer-block__right-text">Фотограф</div>
            <a class="organizer-block__right-site" href="https://vk.com/nyancatic">
              Показать больше информации о фотографе
            </a>
        </div>
        <div>
         <img class="organizer-block__img" src="./assets/img/organizer-block__img.svg">
        </div>
      </div>
      <hr class="line">
    </div>
    <div class="container_main">
      <my-booking></my-booking>
    </div>
    <div class="container_main">
      <div class="reviews-block">
        <div class="reviews-block__title">Отзывы:</div>
        <div class="reviews-block__item">
          <div class="reviews-block__item-wrapper">
            <img class="reviews-block__photo" src="./assets/img/reviews-block__item-1.svg">
            <div class="reviews-block__name-wrapper">
              <p class="reviews-block__name">Валерия Антонова</p>
              <p class="reviews-block__profession">Арт-директор</p>
              <div class="reviews-block__rating">
                <img class="reviews-block__stars" src="./assets/img/text-block-stars.svg">
                <img class="reviews-block__check-mark" src="./assets/img/reviews-block__checkmark.svg">
                <p class="reviews-block__rating-text">Супер! я бы заказала съемку снова!</p>
              </div>
            </div>
          </div>
          <div class="reviews-block__text">
            Хотим выразить огромную благодарность вашей компании!
            Получили море ощущений, все прошло просто замечательно.
            Фотки получились великолепные, отдельное спасибо фотографу!
          </div>
          <div class="reviews-block__date">
            27 Апреля, 2019г.
          </div>
          <hr class="reviews-block__line">
        </div>
        <div class="reviews-block__item">
          <div class="reviews-block__item-wrapper">
            <img class="reviews-block__photo" src="./assets/img/reviews-block__item-2.svg">
            <div class="reviews-block__name-wrapper">
              <p class="reviews-block__name">Виталий Петров</p>
              <p class="reviews-block__profession">Фотограф</p>
              <div class="reviews-block__rating">
                <img class="reviews-block__stars" src="./assets/img/text-block-stars.svg">
                <img class="reviews-block__check-mark" src="./assets/img/reviews-block__checkmark.svg">
                <p class="reviews-block__rating-text">Супер! я бы заказала съемку снова!</p>
              </div>
            </div>
          </div>
          <div class="reviews-block__text">
            Восторг! :) Очень понравилось :) Захватили последний теплый, солнечный октябрьский день :)
            Впечатлило всё: сам вертолет, взлет, полёт, приземление.<br>
            Организация полёта отличная. Спасибо!
          </div>
          <div class="reviews-block__date">
            19 Апреля, 2019г.
          </div>
          <hr class="reviews-block__line">
        </div>
        <div class="reviews-block__item">
          <div class="reviews-block__item-wrapper">
            <img class="reviews-block__photo" src="./assets/img/reviews-block__item-3.svg">
            <div class="reviews-block__name-wrapper">
              <p class="reviews-block__name">Джим Керри</p>
              <p class="reviews-block__profession"></p>
              <div class="reviews-block__rating">
                <img class="reviews-block__stars" src="./assets/img/text-block-stars.svg">
                <img class="reviews-block__check-mark" src="./assets/img/reviews-block__checkmark.svg">
                <p class="reviews-block__rating-text">Супер! я бы заказала съемку снова!</p>
              </div>
            </div>
          </div>
          <div class="reviews-block__text">
            Круто-круто-круто!!! Отмечали мой ДэРэ. Отлично провели время!!! Кстати закуски были вкусными и сытными))Мы
            с собой ничего не брали. Сами много фоткались,поэтому воспоминания обалденные!!!))
            А еще нам всем напечатали по сертификату воздухоплавателя, правда некоторые ленятся за ним съездить)))
            Но все равно приятно. Короче, Презентстар – проверено. Оценка: пять!
          </div>
          <div class="reviews-block__date">
            11 Апреля, 2019г.
          </div>
          <hr class="reviews-block__line">
        </div>
      </div>
    </div>
    <div class="container_footer">
      <div class="footer-block">
        <img class="footer-block__logo-img" src="./assets/img/HELYFLY-logo.svg">
        <div class="footer-block__logo-block">
          <div class="footer-block__logo-block-wrapper">
            <img class="footer-block__logo-block-item" src="./assets/img/footer-block-vk-logo.svg">
            <img class="footer-block__logo-block-item" src="./assets/img/footer-block-fb-logo.svg">
            <img class="footer-block__logo-block-item" src="./assets/img/footer-block-inst-logo.svg">
            <select class="footer-block__languages">
              <option>RU</option>
              <option>EN</option>
            </select>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import myPhoto from "@/components/myPhoto";
import myBooking from "@/components/myBooking";


export default {
  name: 'App',
  components: {
    myPhoto,
    myBooking,
  },

  data() {
    return {
      showText1: false,
      showText2: false,
      text1: true,
      text2: true,
      rotate1: false,
      rotate2: false
    }
  },

  computed: {
    showTextFun1() {
      return this.showText1 ? 'Сначала мы (я и моя команда) изучаем интересы клиентов, а затем придумываем подходящее решение, которое соответствует бюджетуи планам клиента. Мы никогда не зависим от субпоставщиков и не свяжемся' : ''
    },

    showTextFun2() {
      return this.showText2 ? 'При необходимости всегда возможно прерваться на обед/ужин. Качественный подбор места и локации для вашей съемки.' : ''
    },

    textFun1() {
      return this.text1 ? 'Читать дальше' : 'Скрыть текст'
    },

    textFun2() {
      return this.text2 ? 'Читать дальше' : 'Скрыть текст'
    },

    rotateFun1() {
      return this.rotate1 ? 'organizer-block__left-button-symbol' : ''
    },

    rotateFun2() {
      return this.rotate2 ? 'organizer-block__left-button-symbol' : ''
    }
  },

  methods: {
    changeShow1() {
      this.showText1 = !this.showText1
      this.text1 = !this.text1
      this.rotate1 = !this.rotate1
    },

    changeShow2() {
      this.showText2 = !this.showText2
      this.text2 = !this.text2
      this.rotate2 = !this.rotate2
    }
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: "Montserrat-Regular";
  src: url("./assets/fonts/Montserrat-Regular.ttf") format("truetype");
  font-style: normal;
  font-weight: normal;
}

@font-face {
  font-family: "Montserrat-Bold";
  src: url("./assets/fonts/Montserrat-Bold.ttf") format("truetype");
  font-style: normal;
  font-weight: normal;
}

@font-face {
  font-family: "Montserrat-Medium";
  src: url("./assets/fonts/Montserrat-Medium.ttf") format("truetype");
  font-style: normal;
  font-weight: normal;
}

body {
  margin: 0;
}

.container {
  max-width: 1900px;
  margin: auto;

  &_main {
    max-width: 1140px;
    margin: auto;
  }

  &_footer {
    max-width: 990px;
    margin: auto;
  }

  &_gray {
    background-color: #FAF9F8;
  }
}

.header {
  height: 100px;
}

.logo-block{
  display: flex;
  margin-left: 390px;
  padding-top: 39px;
}

.number-phone {
  font-family: Montserrat-Regular;
  font-size: 14px;
  margin: auto;
  margin-left: 36px;

  &_gray {
    color: #B3B3B3;
   }
}

.img-block {
  background-image: url("./assets/img/helicopter.jpg");
  background-position: center center;
  padding-top: 286px;
  padding-bottom: 260px;
  margin-bottom: 70px;

   &__text {
     font-family: Montserrat-Bold;
     font-size: 40px;
     color: #FFFFFF;
     max-width: 890px;
     padding-left: 392px;

     &_orange {
       color: #FC9B09;
     }
   }

  &__price {
    display: flex;
    position: relative;
    margin-top: 29px;
    margin-left: 392px;
  }
}

.price-window {
  position: relative;
}

.price-window-block {
  position: absolute;
  top: 11px;
  left: 22px;
}

.price-window-text {
  font-family: Montserrat-Regular;
  font-size: 20px;
  color: #FFFFFF;
}

.price-window-price {
  font-family: Montserrat-Bold;
  font-size: 35px;
  color: #FFFFFF;
}

.price-window-buttom {
  width: 304px;
  height: 68px;
  font-family: Montserrat-Bold;
  font-weight: 900;
  font-size: 18px;
  color: #FFFFFF;
  border: 3px solid #FFFFFF;
  border-radius: 3px;
  background-color: rgba(1,1,1,0);
  cursor: pointer;
  margin-left: 392px;
}

.symbol-percent {
  position: absolute;
  left: 128px;
  top: 7px;
}

.main-info-block {
  display: flex;
}

.main-info {
  margin-bottom: 40px;

  &__title {
    font-family: Montserrat-Regular;
    font-size: 40px;
    color: #37373F;
    max-width: 250px;
    margin-top: 0;
    margin-bottom: 18px;
  }

  &__text {
    font-family: Montserrat-Regular;
    font-size: 18px;
    color: #37373F;
    max-width: 550px;
    margin-bottom: 21px;
    margin-right: 39px;
  }

  &__item {
    display: flex;
    margin-bottom: 18px;
  }

  &__item-text {
    font-family: Montserrat-Regular;
    font-size: 14px;
    margin-top: auto;
    margin-bottom: auto;
    margin-left: 10px;
  }
}

.main-info-photo {
  max-height: 374px;
}

.text-block {
  max-width: 570px;
  display: flex;
  border-top: 0.5px solid #C7C7C7;
  border-bottom: 0.5px solid #C7C7C7;
  padding-top: 20px;
  padding-bottom: 27px;
  margin-bottom: 30px;

  &__item {
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

.organizer-block {
  display: flex;
  font-family: Montserrat-Regular;
  color: #37373F;
  margin-bottom: 50px;

  &__img {
    padding-top: 18px;
  }

  &__right {
    max-width: 215px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-right: 9px;
  }

  &__right-img {
    max-width: 139px;
    padding-top: 31px;
    margin-bottom: 23px;
  }

  &__right-name {
    font-family: Montserrat-Medium;
    font-size: 18px;
    margin-bottom: 7px;
  }

  &__right-text {
    font-size: 14px;
    margin-bottom: 11px;
  }

  &__right-site {
    display: block;
    text-align: center;
    text-decoration: none;
    font-size: 14px;
    color: #5286EC;
  }

  &__left {
    margin-right: 200px;
  }

  &__left-name {
    font-family: Montserrat-Medium;
    font-size: 18px;
    margin-bottom: 14px;
  }

  &__left-text {
    font-size: 16px;
    max-width: 584px;
    font-weight: 300;
    margin-bottom: 5px;
  }

  &__left-button {
    font-size: 16px;
    border: none;
    background-color: #FFFFFF;
    color: #5286EC;
    cursor: pointer;
    margin-right: 7px;
    padding: 0;

    &_mr {
      margin-bottom: 40px;
    }
  }

  &__left-button-symbol {
    transform: rotate(180deg)
  }
}

.line {
  margin: 0;
  height: 0.5px;
  color: #C7C7C7;
  margin-bottom: 50px;
}

.reviews-block {
  margin-bottom: 150px;

  &__title {
    font-family: Montserrat-Medium;
    font-size: 20px;
    margin-bottom: 50px;
  }

  &__item-wrapper {
    display: flex;
    margin-bottom: 16px;
  }

  &__photo {
    margin-right: 20px;
  }

  &__name-wrapper {
    margin-top: auto;
    margin-bottom: auto;
  }

  &__name {
    font-family: Montserrat-Medium;
    font-size: 18px;
    margin-bottom: 10px;
    color: #37373F;
  }

  &__profession {
    font-family: Montserrat-Regular;
    font-size: 14px;
    margin-bottom: 10px;
    color: #37373F;
  }

  &__rating {
    display: flex;
  }

  &__stars {
    margin-right: 50px;
  }

  &__check-mark {
    margin-right: 5px;
  }

  &__rating-text {
    font-family: Montserrat-Regular;
    font-size: 14px;
    color: #B3B3B3;
  }

  &__text {
    margin-left: 120px;
    margin-bottom: 22px;
    width: 510px;
    font-family: Montserrat-Regular;
    font-size: 16px;
    color: #37373F;
    line-height: 24px;
  }

  &__date {
    margin-left: 120px;
    margin-bottom: 35px;
    font-family: Montserrat-Regular;
    font-size: 14px;
    color: #B3B3B3;
    line-height: 21px;
  }

  &__line {
    width: 510px;
    margin-left: 120px;
    color: #C7C7C7;
    height: 0.5px;
    opacity: 0.5;
    margin-bottom: 30px;
  }
}

.footer-block {
  display: flex;
  justify-content: space-between;
  height: 100px;

  &__logo-img {
    height: 27px;
    margin-top: auto;
    margin-bottom: auto;
  }

  &__logo-block {
    margin-top: auto;
    margin-bottom: auto;
  }

  &__logo-block-wrapper {
    height: 50px;
    display: flex;
  }

  &__logo-block-item {
    margin-left: 30px;
    height: 23px;
    margin-top: auto;
    margin-bottom: auto;
  }

  &__languages {
    margin-left: 30px;
    margin-top: auto;
    margin-bottom: auto;
    height: 23px;
    color: #37373F;
    font-family: Montserrat-Medium;
    font-size: 15px;
    border: none;
  }
}

p {
  margin: 0;
}
</style>
