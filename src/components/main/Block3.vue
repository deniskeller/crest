<template>
  <div class="block3"></div>
</template>
<script>
export default {
  components: {},
};
</script>
<style scoped lang="scss">
.block3 {
  width: 100%;
  height: em(248px);
  background: #c7c7c7;
  @include ifmobile {
    height: em(154px);
  }
}
</style>