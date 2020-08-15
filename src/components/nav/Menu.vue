<template>
  <div class="menu-wrapper">
    <div class="container">
      <div class="menu">
        <div class="menu__mobile">
          <span class="menu__mobile-title">Меню</span>
          <div
            :class="['menu__mobile-burger', {'menu__mobile-burger--open': this.open}]"
            @click="toggleNav"
          ></div>
        </div>
        <div :class="['menu__navbar', {'menu__navbar--open': this.open}]">
          <a class="menu__navbar-item" href="#">О нас</a>
          <a class="menu__navbar-item" href="#">О нас</a>
          <a class="menu__navbar-item" href="#">О нас</a>
          <a class="menu__navbar-item" href="#">О нас</a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {},
  data() {
    return {
      open: false,
    };
  },
  methods: {
    toggleNav() {
      this.open = !this.open;
    },
  },
};
</script>
<style scoped lang="scss">
.menu-wrapper {
  width: 100%;
  background: $yellow;
  .menu {
    width: 100%;
    height: em(58px);
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    position: relative;
    @include ifmobile {
      height: em(50px);
      padding: em(20px);
    }

    &__mobile {
      @include ifdesktop {
        display: none;
      }
      @include ifmobile {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
      }
      &-title {
        font-weight: bold;
        font-size: em(24px);
        line-height: em(28px);
      }
      &-burger {
        display: block;
        width: em(23px);
        height: em(3px);
        background: $black;
        position: relative;
        cursor: pointer;
        &:before,
        &:after {
          content: "";
          display: block;
          position: absolute;
          left: 0;
          min-width: em(23px);
          min-height: em(3px);
          background: $black;
        }
        &:before {
          top: em(-9px);
        }
        &:after {
          top: em(9px);
        }
      }
      &-burger--open {
        background-color: transparent;
        &:before {
          width: em(30px);
          left: -0.15em;
          top: 0;
          transform: rotate(45deg);
        }
        &:after {
          width: em(30px);
          left: -0.15em;
          top: 0;
          transform: rotate(-45deg);
        }
      }
    }

    &__navbar {
      width: 100%;
      height: 100%;
      display: flex;
      @include ifdesktop {
        position: relative;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
      }
      @include ifmobile {
        display: none;
      }
      &-item {
        font-weight: normal;
        font-size: em(24px);
        line-height: em(22px);
        text-transform: uppercase;
        white-space: nowrap;
        padding: 0 em(15px);
      }
    }
    &__navbar--open {
      @include ifmobile {
        display: block;
        position: absolute;
        z-index: 10000;
        left: 0;
        top: em(50px);
        min-height: em(200px);
        background: $yellow;
        display: flex;
        flex-direction: column;
        align-items: center;
      }
    }
  }
}
</style>