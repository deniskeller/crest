<template>
  <div id="app">
    <div class="wrapper-bg">
      <div class="bg"></div>
      <Header />
      <Menu />
      <Content />
    </div>
    <Block2 />
    <Block3 />
    <Footer />
  </div>
</template><script>
import Header from "./components/header/Header.vue";
import Menu from "./components/nav/Menu.vue";
import Content from "./components/main/Content.vue";
import Block2 from "./components/main/Block2.vue";
import Block3 from "./components/main/Block3.vue";
import Footer from "./components/footer/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Menu,
    Content,
    Block2,
    Block3,
    Footer,
  },
};
</script>
<style lang="scss">
#app {
  overflow: hidden;
}
.wrapper-bg {
  width: 100%;
  position: relative;
  // overflow: hidden;

  .bg {
    position: absolute;
    z-index: -1;
    left: calc(50% - 180em);
    bottom: -110.3125em;
    width: 187.5em;
    height: 187.5em;
    border-radius: 50%;
    // transform: rotateZ(4deg);
    color: white;
    background: repeating-linear-gradient(
      135deg,
      #606dbc,
      #606dbc 5px,
      #0c82be 5px,
      #017dc2 20px
    );
    @include ifmobile {
      display: none;
    }
  }
}
</style>