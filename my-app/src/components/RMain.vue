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
            <r-item-service :itemService="itemService" />
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
            <r-item-practice :practiceItemData="item" />
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
          <div class="about__video">
            <iframe
              width="560"
              height="315"
              src="https://www.youtube.com/embed/WSr93jBitwI"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
          <div class="about__content">
            <h2 class="about__title">Most trusted in our field</h2>
            <div class="about__sub-title">
              Most calendars are designed for teams. Slate is designed for
              freelancers who want a simple way to plan their schedule.
            </div>
            <div class="about__items">
              <div class="about__item item-about">
                <div class="item-about__icon">
                  <img src="../assets/images/about/01.svg" alt="about" />
                </div>
                <div class="item-about__body">
                  <div class="item-about__title">
                    the quick fox jumps over the lazy dog
                  </div>
                  <div class="item-about__subtitle">
                    Things on a very small scale ...
                  </div>
                </div>
              </div>
              <div class="about__item item-about">
                <div class="item-about__icon">
                  <img src="../assets/images/about/02.svg" alt="about" />
                </div>
                <div class="item-about__body">
                  <div class="item-about__title">
                    the quick fox jumps over the lazy dog
                  </div>
                  <div class="item-about__subtitle">
                    Things on a very small scale ...
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="page__clients clients">
      <div class="clients__container _container">
        <div class="clients__items">
          <div class="clients__item">
            <img src="../assets/images/clients/01.png" alt="client" />
          </div>
          <div class="clients__item">
            <img src="../assets/images/clients/02.png" alt="client" />
          </div>
          <div class="clients__item">
            <img src="../assets/images/clients/03.png" alt="client" />
          </div>
          <div class="clients__item">
            <img src="../assets/images/clients/04.png" alt="client" />
          </div>
          <div class="clients__item">
            <img src="../assets/images/clients/05.png" alt="client" />
          </div>
          <div class="clients__item">
            <img src="../assets/images/clients/06.png" alt="client" />
          </div>
        </div>
      </div>
    </div>
    <div class="page__subscribe subscribe">
      <div class="subscribe__container _container">
        <div class="subscribe__body">
          <div class="subscribe__title">
            Subscribe For Latest <br />
            Newsletter
          </div>
          <form action="#" class="subscribe__form">
            <input
              class="subscribe__email"
              autocomplete="on"
              type="email"
              name="form"
              required
              placeholder="Your Email"
            />
            <button type="submit" class="subscribe__button">Subscribe</button>
          </form>
        </div>
      </div>
    </div>
    <div class="page__contacts contacts">
      <div class="contacts__container _container">
        <template
          v-for="headerBlockData in headerBlock"
          :key="headerBlockData.id"
        >
          <div v-if="headerBlockData.id === 4">
            <r-header-block :headerBlockDataCh="headerBlockData" />
          </div>
        </template>
        <div class="contacts__items">
          <r-item-contacts
            v-for="contact in contacts"
            :key="contact.id"
            @pushContacts1="pushContacts"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import MyButton1 from "./UI/MyButton1.vue";
import RItemService from "./items/RItemService.vue";
import RHeaderBlock from "./RHeaderBlock.vue";
import RItemPractice from "./items/RItemPractice.vue";
import RItemContacts from "./items/RItemContacts.vue";

export default {
  name: "RMain",
  components: {
    MyButton1,
    RItemService,
    RHeaderBlock,
    RItemPractice,
    RItemContacts,
  },
  data() {
    return {
      headerBlock: [
        {
          id: 1,
          title: "Designing Better Experience",
          description:
            "Problems trying to resolve the conflict between the two major realms \n of Classical physics: Newtonian mechanics",
        },
        {
          id: 2,
          title: "Practice Advice",
          description:
            "Problems trying to resolve the conflict between the two major realms \n of Classical physics: Newtonian mechanics",
        },
        {
          id: 3,
          title: "Who We Are",
          description:
            "Problems trying to resolve the conflict between the two major realms \n of Classical physics: Newtonian mechanics",
        },
        {
          id: 4,
          title: "Get In Touch",
          description:
            "Problems trying to resolve the conflict between the two major realms \n of Classical physics: Newtonian mechanics",
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
      contacts: [],
    };
  },
  props: {
    itemsService: {
      type: Array,
      required: true,
    },
  },
  methods: {
    pushContacts(contacts) {
      console.log(contacts);
    },
  },
  mounted() {},
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
  &__clients {
    padding: 40px 0;
  }
  &__subscribe {
    padding-bottom: 40px;
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
    margin-top: 50px;
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

//=====================о нас=================================================
.about {
  &__container {
  }

  &__body {
    display: flex;
    margin-top: 50px;
  }

  &__video {
    flex: 0 0 55%;
    position: relative;
    padding: 0 57% 42.25% 0;
  }

  &__video iframe {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    object-fit: cover;
  }

  &__content {
    flex: 1 1 auto;
    margin-left: 20px;
  }

  &__title {
    font-weight: 700;
    font-size: 40px;
    line-height: 57px;
    letter-spacing: 0.2px;
    color: #252b42;

    margin-bottom: 10px;
  }

  &__sub-title {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.2px;
    color: #737373;
  }

  &__items {
    > *:not(:last-child) {
      margin-bottom: 20px;
    }
    margin-top: 40px;
  }

  @media (max-width: 770px) {
    &__body {
      flex-wrap: wrap;
    }

    &__video {
      flex: 0 0 100%;
      margin-bottom: 20px;
    }

    &__content {
      margin-left: 0;
    }
  }

  @media (max-width: 516px) {
    & > *:not(:last-child) {
      margin-bottom: 10px;
    }

    &__body {
      margin-top: 35px;
    }

    &__title {
      margin-bottom: 5px;
    }

    &__items {
      > *:not(:last-child) {
        margin-bottom: 10px;
      }
      margin-top: 20px;
    }
  }

  &__item {
  }
}
.item-about {
  display: flex;

  &__icon {
    margin-right: 20px;
  }

  &__body {
    flex: 1 1 auto;
  }

  &__title {
    font-weight: 700;
    font-size: 16px;
    line-height: 150%;
    letter-spacing: 0.1px;
  }

  &__subtitle {
    font-weight: 600;
    font-size: 14px;
    line-height: 24px;
    letter-spacing: 0.2px;
    color: #737373;
  }
}

//==================clients-==================
.clients {
  &__container {
  }

  &__items {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

  &__item {
    padding: 8px 10px;
    flex: 0 1 16.6667%;
    text-align: center;
    min-width: 140px;
  }

  @media (max-width: 770px) {
    & {
      padding-top: 0;
    }
  }
}

//=========subscribe=======================
.subscribe {
  &__container {
  }

  &__body {
    display: flex;
    align-items: center;
    margin: 0 30px;
    background: #17213c;
    padding: 30px 40px;
    border-radius: 2px;
  }

  &__title {
    flex: 0 1 50%;

    font-weight: 700;
    font-size: 24px;
    line-height: 133%;
    letter-spacing: 0.1px;
    color: #ffffff;
  }

  &__form {
    flex: 0 1 50%;
    display: flex;
    align-items: center;
  }

  &__email {
    display: flex;
    align-items: center;
    padding-left: 15px;
    flex: 1 1 auto;
    min-height: 60px;
    background: #f9f9f9;
    border: 1px solid #e6e6e6;
    border-radius: 5px 0 0 5px;
  }

  &__button {
    padding: 15px 22px;

    background: #ff7b47;
    border: 1px solid #e6e6e6;
    border-radius: 0px 5px 5px 0px;

    font-weight: 400;
    font-size: 14px;
    line-height: 200%;
    text-align: center;
    letter-spacing: 0.2px;
    color: #ffffff;

    cursor: pointer;
  }
}
</style>