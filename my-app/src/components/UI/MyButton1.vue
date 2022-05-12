<template>
  <a class="button1" href="">
    <slot></slot>
  </a>
</template>

<script>
export default {
  name: "MyButton1",
};
</script>

<style lang="scss">
.button1 {
  border: 1px solid #0d5c63;
  border-radius: 37px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px 36px;
  color: #0d5c63;
  text-align: center;
  font-weight: 700;
  font-size: 14px;
  line-height: 200%;
  letter-spacing: 0.2px;
  &:hover {
    background: #ff7b47;
    color: #ffffff;
    border: 1px solid #ff7b47;
  }
}
</style>