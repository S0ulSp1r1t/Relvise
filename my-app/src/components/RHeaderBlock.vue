<template>
  <div class="advantages__header header-block">
    <h2 class="header-block__title">{{ headerBlockDataCh.title }}</h2>
    <div class="header-block__description">
      {{ headerBlockDataCh.description }}
    </div>
  </div>
</template>

<script>
export default {
  name: "RHeaderBlock",
  props: {
    headerBlockDataCh: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.header-block {
  & > * :not(:last-child) {
    margin-bottom: 10px;
  }
  letter-spacing: 0.2px;
  text-align: center;

  &__title {
    line-height: 142%;
    font-weight: 700;
    font-size: 40px;
    margin-bottom: 10px;
  }

  &__description {
    font-style: normal;
    line-height: 142%;
    font-weight: 500;
    font-size: 14px;
    color: #737373;
  }
}
</style>