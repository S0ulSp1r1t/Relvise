<template>
  <main class="page">
    <div class="page__main-block main-block">
      <div class="main-block__container _container">
        <div class="main-block__body">
          <h1 class="main-block__title">Finance and Consultancy Solution</h1>
          <h4 class="main-block__description">
            We know how large objects will act, but things on a small scale.
          </h4>
          <div class="main-block__btns">
            <my-button-1 class="main-block__my-button-1"
              >Get Quote Now</my-button-1
            >
            <my-button-1 class="main-block__my-button-1"
              >Learn More</my-button-1
            >
          </div>
        </div>
      </div>
      <div class="main-block__image _ibg" style="position: absolute">
        <img src="../assets/images/background.jpg" alt="background" />
      </div>
    </div>
    <section class="page__services services">
      <div class="services__container _container">
        <div class="services__body">
          <div
            class="services__column"
            v-for="itemService in itemsService"
            :key="itemService.id"
          >
            <r-item-service v-bind:itemService="itemService" />
          </div>
        </div>
      </div>
    </section>
    <section class="page__advantages advantages">
      <div class="advantages__container _container">
        <template
          v-for="headerBlockData in headerBlock"
          :key="headerBlockData.id"
        >
          <div v-if="headerBlockData.id === 1">
            <r-header-block :headerBlockDataCh="headerBlockData" />
          </div>
        </template>
        <div class="advantages__body">
          <div class="advantages__column">
            <div class="advantages__item">
              <div class="advantages__icon">
                <img src="../assets/images/advantages/01.svg" alt="advantage" />
              </div>
              <h2 class="advantages__value">972 +</h2>
              <div class="advantages__text">Consumer Products</div>
            </div>
          </div>
          <div class="advantages__column">
            <div class="advantages__item">
              <div class="advantages__icon">
                <img src="../assets/images/advantages/02.svg" alt="advantage" />
              </div>
              <h2 class="advantages__value">181 +</h2>
              <div class="advantages__text">Financia Services</div>
            </div>
          </div>
          <div class="advantages__column">
            <div class="advantages__item">
              <div class="advantages__icon">
                <img src="../assets/images/advantages/03.svg" alt="advantage" />
              </div>
              <h2 class="advantages__value">98%</h2>
              <div class="advantages__text">Environmental</div>
            </div>
          </div>
          <div class="advantages__column">
            <div class="advantages__item">
              <div class="advantages__icon">
                <img src="../assets/images/advantages/04.svg" alt="advantage" />
              </div>
              <h2 class="advantages__value">746 +</h2>
              <div class="advantages__text">Business & Finance</div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="page__practice practice">
      <div class="practice__container _container">
        <template
          v-for="headerBlockData in headerBlock"
          :key="headerBlockData.id"
        >
          <div v-if="headerBlockData.id === 2">
            <r-header-block :headerBlockDataCh="headerBlockData" />
          </div>
        </template>
        <div class="practice__body">
          <div
            class="practice__column"
            v-for="item in practiceItem"
            :key="item.id"
          >
            <r-practice-item :practiceItemData="item" />
          </div>
        </div>
      </div>
    </section>
    <section class="page__about about">
      <div class="about__container _container">
        <template
          v-for="headerBlockData in headerBlock"
          :key="headerBlockData.id"
        >
          <div v-if="headerBlockData.id === 3">
            <r-header-block :headerBlockDataCh="headerBlockData" />
          </div>
        </template>
        <div class="about__body">
          <div class="about__video"></div>
          <div class="about__content">
            <div class="about__description">
              <div class="about__title"></div>
              <div class="about__subtitle"></div>
            </div>
            <div class="about__items">
              <div class="about__item item-about">
                <div class="item-about__title">
                  <div class="item-about__subtitle"></div>
                </div>
              </div>
              <div class="about__item item-about">
                <div class="item-about__title">
                  <div class="item-about__subtitle"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import MyButton1 from "./UI/MyButton1.vue";
import RItemService from "./RItemService.vue";
import RHeaderBlock from "./RHeaderBlock.vue";
import RPracticeItem from "./RPracticeItem.vue";

export default {
  name: "RMain",
  components: {
    MyButton1,
    RItemService,
    RHeaderBlock,
    RPracticeItem,
  },
  data() {
    return {
      headerBlock: [
        {
          id: 1,
          title: "Designing Better Experience",
          description:
            "Problems trying to resolve the conflict between the two major realms" +
            <br /> +
            "of Classical physics: Newtonian mechanics",
        },
        {
          id: 2,
          title: "Practice Advice",
          description:
            "Problems trying to resolve the conflict between the two major realms" +
            <br /> +
            "of Classical physics: Newtonian mechanics",
        },
        {
          id: 3,
          title: "Who We Are",
          description:
            "Problems trying to resolve the conflict between the two major realms" +
            <br /> +
            "of Classical physics: Newtonian mechanics",
        },
        {
          id: 4,
          title: "Get In Touch",
          description:
            "Problems trying to resolve the conflict between the two major realms" +
            <br /> +
            "of Classical physics: Newtonian mechanics",
        },
      ],
      practiceItem: [
        {
          id: 1,
          title: "A single source of truth",
          description:
            "Newton thought that light was made up of particles, but then it was discovered ",
          img: "01.jpg",
        },
        {
          id: 2,
          title: "Fastest way to organize",
          description:
            "“Quantum mechanics” is the description of the behaviour of matter",
          img: "02.jpg",
        },
        {
          id: 3,
          title: "Fastest way to take action",
          description: "They describe a universe consisting of bodies moving",
          img: "03.jpg",
        },
        {
          id: 4,
          title: "Work better together",
          description:
            "They finally obtained a consistent description of the behaviour",
          img: "04.jpg",
        },
      ],
    };
  },
  props: {
    itemsService: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
body {
  background: #fafafa;
}

//--------------страницы-----------------------------------------------------------------------------
.page {
  flex: 1 1 auto;
  &:hover {
    cursor: default;
  }
  &__main-block {
  }
  &__services {
    padding-bottom: 40px;
  }
  &__advantages {
    padding: 40px 0;
  }
  &__practice {
    padding: 40px 0;
  }
  &__about {
    padding: 40px 0;
  }
}

//--------------хедер-----------------------------------------------------------------------------

//--------------мэйн блок-----------------------------------------------------------------------------
.main-block {
  position: relative;
  &__container {
  }

  &__body {
    padding-top: 184px;
    padding-bottom: 191px;
    max-width: 400px;
    > *:not(:last-child) {
      margin-bottom: 35px;
    }
  }

  @media (max-width: 992px) {
    &__body {
      padding-top: 120px;
    }
  }

  &__title {
    font-weight: 800;
    font-size: 58px;
    line-height: 137%;
  }

  @media (max-width: 479px) {
    &__title {
      font-size: 48px;
    }
  }

  @media (max-width: 342px) {
    &__title {
      font-size: 40px;
    }
  }

  &__description {
    font-weight: 500;
    font-size: 20px;
    line-height: 150%;
    letter-spacing: 0.2px;
    color: #737373;
  }

  &__btns {
    display: inline-flex;
    flex-wrap: wrap;
    margin: -10px 0;
  }

  &__image {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: -100;
  }

  @media (max-width: 992px) {
    &__image {
      opacity: 0.5;
    }
  }

  @media (max-width: 1300px) {
    &__image img {
      object-position: right;
    }
  }
}

.main-block__my-button-1 {
  margin: 10px 0;

  @media (max-width: 390px) {
    & {
      flex: 1 1 100%;
    }
  }

  @media (min-width: 390px) {
    &:not(:last-child) {
      margin-right: 10px;
    }
  }
}
//--------------сервис блок-----------------------------------------------------------------------------
.services {
  position: relative;
  margin-top: -111px;
  z-index: 2;

  &__container {
  }

  &__body {
    display: flex;
    margin: 0 -15px -20px;
    flex-wrap: wrap;
  }

  &__column {
    padding: 0 15px;
    flex: 0 1 33.3333%;
    margin-bottom: 20px;
  }

  @media (max-width: 992px) {
    &__column {
      flex: 0 1 50%;
    }

    &__column:last-child {
      flex: 0 1 100%;
    }
  }

  @media (max-width: 652px) {
    &__column {
      flex: 0 1 100%;
    }
  }

  &__item {
  }
}

//--------------заслуги блок-----------------------------------------------------------------------------

.advantages {
  &__container {
  }

  &__header {
  }

  &__body {
    display: flex;
    //justify-content: center;
    margin-top: 50px;
    flex-wrap: wrap;
    padding: 0 -15px;
  }

  &__column {
    padding: 0 15px;
    flex: 0 1 25%;
  }

  @media (max-width: 1064px) and (min-width: 808px) {
    &__column {
      flex: 0 1 33.333%;
    }
    &__column:last-child {
      flex: 0 1 100%;
    }
  }

  @media (max-width: 806px) and (min-width: 550px) {
    &__column {
      flex: 0 1 50%;
    }
  }

  @media (max-width: 548px) {
    &__column {
      flex: 0 1 100%;
    }
  }

  &__item {
    padding: 30px;
    text-align: center;
    box-shadow: 0px 13px 19px rgba(0, 0, 0, 0.07);
    &__item > * :not(:last-child) {
      margin-bottom: 10px;
    }
  }

  &__icon {
  }

  &__value {
    font-weight: 700;
    font-size: 40px;
    line-height: 142%;
    letter-spacing: 0.2px;
  }

  &__text {
    font-weight: 700;
    font-size: 16px;
    line-height: 150%;
    letter-spacing: 0.1px;
    color: #737373;
  }
}

//--------------практика блок-----------------------------------------------------------------------------
.practice {
  &__container {
  }

  &__header-block {
  }

  &__body {
    display: flex;
    margin-top: 45px;
    padding: 0 -20px;
    flex-wrap: wrap;
  }

  &__column {
    flex: 0 1 25%;
    padding: 0 20px;
  }

  @media (max-width: 892px) {
    &__column {
      flex: 0 1 50%;
    }
  }

  @media (max-width: 546px) {
    &__column {
      flex: 0 1 100%;
    }
  }
}
</style>