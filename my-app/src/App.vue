<template>
  <div class="wrapper">
    <r-header />
    <r-main />
    <r-footer />
  </div>
</template>

<script>
import RFooter from "./components/RFooter.vue";
import RHeader from "./components/RHeader.vue";
import RMain from "./components/RMain.vue";

export default {
  name: "App",
  components: {
    RHeader,
    RFooter,
    RMain,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/css/nullstyle.css";

.wrapper {
  display: flex;
  flex-direction: column;
  overflow: hidden;
  min-height: 100%;
}
._container {
  margin: 0 auto;
  max-width: 1046px;
  box-sizing: content-box;
  padding: 0 15px;
}
._ibg {
}
._ibg img {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  object-fit: cover;
}
</style>
