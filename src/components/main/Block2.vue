<template>
  <div class="block2"></div>
</template>
<script>
export default {
  components: {},
};
</script>
<style scoped lang="scss">
.block2 {
  width: 100%;
  height: em(248px);
  background: #9b9a99;
  @include ifmobile {
    height: em(154px);
  }
}
</style>