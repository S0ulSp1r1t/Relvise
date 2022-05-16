<template>
  <div class="services__item item-service">
    <div class="item-service__icon">
      <img
        :src="require('@/assets/images/service/' + itemService.svg)"
        alt="service"
      />
    </div>
    <h3 class="item-service__title">{{ itemService.title }}</h3>
    <div class="item-service__description">
      {{ itemService.description }}
    </div>
  </div>
</template>

<script>
export default {
  name: "RItemService",
  props: {
    itemService: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.item-service {
  box-shadow: 0px 13px 19px rgba(0, 0, 0, 0.07);
  padding: 35px 40px;
  background: rgb(255, 255, 255);

  &__icon {
  }

  &__title {
    font-weight: 700;
    font-size: 24px;
    line-height: 133%;
    letter-spacing: 0.1px;
    color: #252b42;
  }

  &__description {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.2px;
    color: #737373;
  }

  &:hover {
    background: #0d5c63;
    cursor: pointer;
    img {
      filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg)
        brightness(102%) contrast(102%);
    }
    h3,
    div {
      color: #fff;
    }
  }
}
</style>