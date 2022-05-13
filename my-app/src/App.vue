<template>
  <div class="wrapper">
    <r-header />
    <r-main :itemsService="itemsService" />
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
  data() {
    return {
      itemsService: [
        {
          id: 1,
          svg: "01.svg",
          title: "Environmental Consulting",
          description: "We focus on ergonomics and meeting you where you work.",
        },
        {
          id: 2,
          svg: "02.svg",
          title: "Finance and consultancy ",
          description: "Just type what's on your mind and we'll get you there.",
        },
        {
          id: 3,
          svg: "03.svg",
          title: "Financial Services Consulting",
          description: "the quick fox jumps over the lazy dog",
        },
      ],
    };
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
  position: relative;
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
