<template>
  <div class="main-wrapper">
    <div class="container">
      <div class="main">
        <div class="left-content">
          <h2 class="left-content__title">
            ОФИЦИАЛЬНЫЙ ПРОИЗВОДИТЕЛЬ
            <span class="yellow">Текст, текст, текст</span>
          </h2>
          <img
            class="left-content__img left-content__img--desktop"
            src="@/assets/img/prise-white.svg"
            alt
          />
          <img
            class="left-content__img left-content__img--mobile"
            src="@/assets/img/prise-black.svg"
            alt
          />
          <div class="left-content__subtitle">*средних по Тольятти</div>
          <div class="left-content__free">
            <img src="@/assets/img/roulette.svg" alt class="free-img" />
            <div class="free-title">
              <div class="bold">БЕСПЛАТНЫЙ</div>ВЫЕЗД ЗАМЕРЩИКА
            </div>
            <div class="free-subtitle">
              <span class="triangle"></span>ВЫЕЗЖАЕМ В ДЕНЬ ОБРАЩЕНИЯ
            </div>
          </div>
        </div>
        <div class="right-content">
          <img src="@/assets/img/kbe.svg" alt class="right-content__kbe" />
          <img src="@/assets/img/rehau.svg" alt class="right-content__rehau" />
          <div class="right-content__text">
            <img src="@/assets/img/calc.svg" alt />
            <p>Получить точный расчёт И СРАВНИТЬ ЦЕНЫ</p>
          </div>
          <img class="right-content__man" src="@/assets/img/man.svg" alt />
        </div>
      </div>
    </div>
    <div class="main-wrapper__bg"></div>
    <div class="main-wrapper__payment">
      <img class="visa" src="@/assets/img/visa.svg" alt />
      <img class="mastercard" src="@/assets/img/mastercard.svg" alt />
      <img class="sberbank" src="@/assets/img/sberbank.svg" alt />
    </div>
  </div>
</template>
<script>
export default {
  components: {},
};
</script>
<style scoped lang="scss">
.main-wrapper {
  min-height: em(544px);
  position: relative;

  &__payment {
    position: absolute;
    bottom: em(61px);
    right: em(22px);
    @include ifmobile {
      display: none;
    }
    img {
      margin-right: em(11px);
    }
    .visa {
      width: em(74px);
      height: em(43px);
    }
    .mastercard {
      width: em(74px);
      height: em(43px);
    }
    .sberbank {
      width: em(178px);
      height: em(43px);
    }
  }
  .main {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: em(82px) em(20px) em(95px);
    @include ifmobile {
      flex-direction: column;
      justify-content: center;
      padding: em(279px) em(20px) em(78px);
    }
    .left-content {
      display: flex;
      flex-direction: column;
      @include ifmobile {
        align-items: center;
      }
      &__title {
        width: em(160px);
        font-size: em(40px);
        line-height: em(20px);
        font-weight: 900;
        margin-bottom: em(18px);
        color: $white;
        span.yellow {
          color: $yellow;
          @include ifdesktop {
            text-transform: uppercase;
          }
        }

        @include ifmobile {
          font-size: em(32px);
          color: $black;
          text-align: center;
          text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.25);
          span.yellow {
            color: $orange;
          }
        }
      }
      &__subtitle {
        position: relative;
        top: em(-8px);
        font-weight: bold;
        font-size: em(24px);
        line-height: em(28px);
        color: $white;
        transform: rotate(-3deg);
        margin-left: em(22px);
        @include ifmobile {
          color: $black;
          margin-left: em(-16px);
        }
      }
      &__img--desktop {
        width: em(411px);
        height: em(100px);
        @include ifmobile {
          display: none;
        }
      }
      &__img--mobile {
        display: none;
        width: em(307px);
        height: em(66px);
        @include ifmobile {
          display: block;
        }
      }
      &__free {
        width: 100%;
        max-width: em(345px);
        height: em(60px);
        background: linear-gradient(266.8deg, #fff854 0.02%, #ffe03e 101.17%);
        color: $black;
        position: relative;
        border-radius: em(6px);
        padding: em(6px) em(32px) em(6px) em(84px);
        margin-top: em(20px);
        @include ifdesktop {
          display: none;
        }

        .free-img {
          position: absolute;
          left: em(5px);
          bottom: 0;
          width: em(63px);
          height: em(49px);
        }
        .free-title {
          font-weight: bold;
          font-size: em(16px);
          line-height: em(19px);
          letter-spacing: 0.3em;
          white-space: nowrap;
          .bold {
            font-weight: 900;
            font-size: em(24px);
            line-height: em(19px);
            letter-spacing: 0.27em;
          }
        }
        .free-subtitle {
          position: absolute;
          bottom: em(-38px);
          left: calc(50% - 8.5em);
          border: em(1.5px) solid #f26422;
          padding: em(7px);
          border-radius: 4px;
          font-weight: bold;
          font-size: em(14px);
          line-height: em(16px);
          color: $orange;
          span.triangle {
            width: em(18px);
            height: 0.3125em;
            display: block;
            position: absolute;
            background: #ffffff;
            top: -0.0875em;
            left: calc(50% - 0.5em);
            border-bottom: 0.2125em solid #fff;
          }
          &::before,
          &::after {
            content: "";
            display: block;
            position: absolute;
            width: em(16px);
            background: $white;
            border-top: em(1.5px) solid $orange;
          }
          &:before {
            top: -0.4em;
            left: calc(50% - 0.2em);
            transform: rotate(-134deg);
            z-index: 1;
          }
          &:after {
            top: -0.4em;
            left: calc(50% - 0.8em);
            transform: rotate(133deg);
          }
        }
      }
    }
    .right-content {
      width: 100%;
      position: relative;
      img {
        position: absolute;
      }
      &__man {
        right: calc(50% - 34em);
        bottom: em(-96px);
        width: em(484px);
        height: em(514px);
        @include ifmobile {
          width: em(194px);
          height: em(187px);
          right: calc(50% - 12em);
          bottom: 0;
          top: em(-575px);
        }
      }
      &__kbe {
        right: calc(50% - 4em);
        top: em(16px);
        width: em(134px);
        height: em(85px);
        @include ifmobile {
          width: em(94px);
          height: em(61px);
          right: calc(50% - 1em);
          top: -33.8375em;
        }
      }
      &__rehau {
        right: calc(50% - -6.3em);
        top: em(2px);
        width: em(94px);
        height: em(98px);
        @include ifmobile {
          width: em(68px);
          height: em(70px);
          width: 4.25em;
          height: 4.375em;
          right: calc(50% - -6em);
          top: -34.0375em;
        }
      }
      &__text {
        position: absolute;
        z-index: 1000;
        bottom: em(-135px);
        right: em(-35px);
        width: em(390px);
        height: em(90px);
        background: $orange;
        border: em(6px) solid $white;
        border-radius: 10px;
        overflow: hidden;
        padding: em(16px) em(30px) em(13px) em(80px);
        display: flex;
        align-items: center;
        padding-left: em(80px);
        @include ifmobile {
          display: none;
        }
        img {
          display: block;
          width: em(43px);
          height: em(50px);
          position: absolute;
          left: em(30px);
          bottom: em(17px);
        }
        p {
          display: block;
          width: em(230px);
          font-weight: 900;
          // font-size: em(19px);
          line-height: em(22px);
          color: $white;
          text-transform: uppercase;
        }
      }
    }
  }
  &__bg {
    position: absolute;
    z-index: -1000;
    top: 0;
    right: 0;
    width: 100%;
    height: 100%;
    display: block;
    background: url("../../assets/img/background.png") no-repeat;
    background-position: 100%;
    background-size: contain;
    @include ifmobile {
      height: em(181px);
      background-size: cover;
      background-position: top;
    }
    @include respondFrom(2400px) {
      background-size: cover;
    }
  }
}
</style>