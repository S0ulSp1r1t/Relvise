<template>
  <div class="item-contacts">
    <div class="item-contacts__logo">
      <img
        :src="required('@/assets/images/contacts') + services.logo"
        alt="contacts"
      />
    </div>
    <div class="item-contacts__mail">{{ services.email_1 }}</div>
    <div class="item-contacts__action-text">{{ services.email_2 }}</div>
    <button class="item-contacts__button" type="submit">Submit Request</button>
  </div>
</template>

<script>
export default {
  name: "RItemContacts",
  data() {
    return {
      contacts: [
        {
          id: 1,
          logo: "01.svg",
          email_1: "georgia.young@example.com",
          email_2: "georgia.young@ple.com",
          action: "Get Support",
        },
        {
          id: 2,
          logo: "02.svg",
          email_1: "georgia.young@example.com",
          email_2: "georgia.young@ple.com",
          action: "Get Support",
        },
        {
          id: 3,
          logo: "03.svg",
          email_1: "georgia.young@example.com",
          email_2: "georgia.young@ple.com",
          action: "Get Support",
        },
      ],
    };
  },
  methods: {
    pushContacts() {
      this.$emit("pushContacts1", this.contacts);
    },
  },
  mounted() {
    this.pushContacts;
  },
};
</script>

<style lang="scss" scoped>
</style>