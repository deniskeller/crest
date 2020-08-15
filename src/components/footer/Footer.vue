<template>
  <div class="wrapper-footer">
    <div class="container">
      <div class="footer">
        <div class="footer__logo">
          <div class="logo">
            <div class="logo__overlay">
              <img class="logo__img" src="@/assets/img/percent.svg" alt />
              <div class="logo__title">текст</div>
            </div>
          </div>
        </div>
        <div class="footer__title">подвал</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
};
</script>
<style scoped lang="scss">
.wrapper-footer {
  width: 100%;
  background: #015a76;
  .footer {
    width: 100%;
    min-height: em(120px);
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-left: em(20px);
    padding-right: em(20px);
    @include ifmobile {
      justify-content: center;
      min-height: em(378px);
    }
    &__logo {
      width: em(168px);
      height: em(61px);
      background: $orange;
      position: relative;
      box-shadow: 2px 2px 3px rgba(0, 0, 0, 0.25);
      padding: em(5px);
      @include ifmobile {
        display: none;
      }
      .logo {
        width: 100%;
        height: 100%;
        border: 1px dashed $white;
        &__overlay {
          position: relative;
          width: 100%;
          height: 100%;
          display: flex;
          align-items: center;
          padding-left: em(70px);
        }
        &__img {
          width: em(35px);
          height: em(35px);
          position: absolute;
          left: em(13px);
        }
        &__title {
          font-weight: 900;
          font-size: em(21px);
          color: $white;
          text-transform: uppercase;
        }
      }
    }
    &__title {
      font-weight: bold;
      font-size: em(22px);
      color: $white;
      text-transform: uppercase;
      margin-left: em(342px);
      @include ifmobile {
        margin-left: 0;
      }
    }
  }
}
</style>