<template>
  <div class="item-contacts">
    <div class="item-contacts__logo">
      <img
        :src="require('@/assets/images/contacts/' + contact.logo)"
        alt="contacts"
      />
    </div>
    <div class="item-contacts__mail">{{ contact.email_1 }}</div>
    <div class="item-contacts__action-text">{{ contact.email_2 }}</div>
    <button class="item-contacts__button" type="submit">Submit Request</button>
  </div>
</template>

<script>
export default {
  name: "RItemContacts",
  props: {
    contact: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.item-contacts {
  padding: 50px 40px;
  text-align: center;
  > *:not(:last-child) {
    padding-bottom: 15px;
  }
  &__logo {
  }

  &__mail {
    font-weight: 600;
    font-size: 14px;
    line-height: 171%;
    text-align: center;
    letter-spacing: 0.2px;
  }

  &__action-text {
    font-weight: 700;
    font-size: 16px;
    line-height: 150%;
    text-align: center;
    letter-spacing: 0.1px;
  }

  &__button {
    padding: 10px 20px;
    border: 1px solid #ff7b47;
    border-radius: 5px;

    font-weight: 600;
    font-size: 14px;
    line-height: 171%;
    text-align: center;
    letter-spacing: 0.2px;
    color: #ff7b47;

    cursor: pointer;
  }

  &:hover {
    background: #252b42;
    padding: 80px 40px;
    div,
    button {
      color: #ffff;
      background: #252b42;
    }
    img {
      filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg)
        brightness(102%) contrast(102%);
    }
  }
}
</style>