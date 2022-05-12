<template>
  <header class="header">
    <div class="header__container _container">
      <a href="" class="header__logo">Relvise</a>
      <nav class="header__menu menu">
        <ul class="menu__list">
          <li class="menu__item">
            <a href="" class="menu__link">Home</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">Product</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">Pricing</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">Contact</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "RHeader",
};
</script>

<style lang="scss">
.header {
  position: absolute;
  width: 100%;
  left: 0;
  top: 0;
  z-index: 50;
  &__container {
    min-height: 104px;
    display: flex;
    align-items: center;
  }
  @media (max-width: 479px) {
    &__container {
      min-height: 70px;
    }
  }
  &__logo {
    font-weight: 700;
    font-size: 24px;
    letter-spacing: 0.1px;
  }
  &__menu {
    margin-left: 132px;
  }
  @media (max-width: 992px) {
    &__menu {
      margin-left: 80px;
    }
  }
  @media (max-width: 768px) {
    &__menu {
      margin-left: 50px;
    }
  }
  @media (max-width: 479px) {
    &__menu {
      margin-left: 15px;
    }
  }
}

.menu {
  padding: 5px;
  &__list {
    display: flex;
    flex-wrap: wrap;
  }
  &__item {
  }
  &__item:not(:last-child) {
    margin-right: 21px;
  }
  &__link {
    color: #737373;
    letter-spacing: 0.2px;
    line-height: 171%;
    font-weight: 600;
  }
  @media (max-width: 479px) {
    &__link {
      letter-spacing: 0.1px;
      font-size: 18px;
    }
  }
}
</style>