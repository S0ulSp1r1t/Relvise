<template>
  <div class="practice__item item-practice">
    <div class="item-practice__text-container">
      <h5 class="item-practice__title">{{ practiceItemData.title }}</h5>
      <div class="item-practice__description">
        {{ practiceItemData.description }}
      </div>
    </div>
    <div class="item-practice__img _ibg">
      <img
        :src="require('@/assets/images/practice/' + practiceItemData.img)"
        alt="practice"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "RPracticeItem",
  props: {
    practiceItemData: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.item-practice {
  display: flex;
  flex-direction: column;
  height: 100%;

  &__text-container {
    padding: 30px;
    flex: 1 1 auto;
    > *:not(:last-child) {
      padding-bottom: 15px;
    }
  }

  @media (max-width: 892px) {
    &__text-container {
      padding: 30px 20px 20px 20px;
      > *:not(:last-child) {
        padding-bottom: 10px;
      }
    }
  }

  @media (max-width: 546px) {
    &__text-container {
      padding: 30px 10px 10px 10px;
      > *:not(:last-child) {
        padding-bottom: 5px;
      }
    }
  }

  &__title {
    font-weight: 700;
    font-size: 16px;
    line-height: 142%;
    letter-spacing: 0.1px;
    margin: 0;
  }

  &__description {
    font-weight: 500;
    font-size: 14px;
    line-height: 142%;
    letter-spacing: 0.2px;
  }

  &__img {
    display: block;
    padding: 0 0 60% 0;
  }
}
</style>