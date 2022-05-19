<template>
  <footer class="footer">
    <div class="footer__footer-top footer-top">
      <div class="footer-top__container _container">
        <div class="footer-top__column">
          <div class="footer-top__label">Company Info</div>
          <nav class="footer-top__menu-footer menu-footer">
            <ul class="menu-footer__list">
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">About Us</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Carrier</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">We are hiring</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Blog</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="footer-top__column">
          <div class="footer-top__label">Legal</div>
          <nav class="footer-top__menu menu-footer">
            <ul class="menu-footer__list">
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">About Us</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Carrier</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">We are hiring</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Blog</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="footer-top__column">
          <div class="footer-top__label">Features</div>
          <nav class="footer-top__menu menu-footer">
            <ul class="menu-footer__list">
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Business Marketing</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">User Analytic</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Live Chat</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Unlimited Support</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="footer-top__column">
          <div class="footer-top__label">Resources</div>
          <nav class="footer-top__menu menu-footer">
            <ul class="menu-footer__list">
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">IOS & Android</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Watch a Demo</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">Customers</a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">API</a>
              </li>
            </ul>
          </nav>
        </div>
        <div class="footer-top__column">
          <div class="footer-top__label">Get In Touch</div>
          <nav class="footer-top__menu menu-footer">
            <ul class="menu-footer__list">
              <li class="menu-footer__item">
                <a href="tel:4805550103" class="menu-footer__link">
                  <img
                    src="@/assets/images/footer_top/01.svg"
                    alt="footer-top"
                    class="menu-footer__icon"
                  />
                  <div>(480) 555-0103</div>
                </a>
              </li>
              <li class="menu-footer__item">
                <a href="" class="menu-footer__link">
                  <img
                    src="@/assets/images/footer_top/02.svg"
                    alt="footer-top"
                    class="menu-footer__icon"
                  />
                  <div
                    style="
                      max-width: 240px;
                      overflow: hidden;
                      white-space: nowrap;
                      text-overflow: ellipsis;
                    "
                  >
                    4517 Washington Ave. Manchester, Kentucky 39495
                  </div>
                </a>
              </li>
              <li class="menu-footer__item">
                <a
                  href="mailto:debra.holt@example.com"
                  class="menu-footer__link"
                >
                  <img
                    src="@/assets/images/footer_top/03.svg"
                    alt="footer-top"
                    class="menu-footer__icon"
                  />
                  <div>debra.holt@example.com</div>
                </a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
    <div class="footer__footer-bottom footer-bottom">
      <div class="footer-bottom__container _container">
        <div class="footer-bottom__made-by">
          Made With Love By Figmaland All Right Reserved
        </div>
        <div class="footer-bottom__socials">
          <div class="footer-bottom__img">
            <img src="@/assets/images/footer_bottom/01.svg" alt="" />
          </div>
          <div class="footer-bottom__img">
            <img src="@/assets/images/footer_bottom/02.svg" alt="" />
          </div>
          <div class="footer-bottom__img">
            <img src="@/assets/images/footer_bottom/03.svg" alt="" />
          </div>
          <div class="footer-bottom__img">
            <img src="@/assets/images/footer_bottom/04.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "RFooter",
};
</script>

<style lang="scss">
.footer {
  &__footer-top {
    padding: 50px 0;
  }

  @media (max-width: 704px) {
    padding-top: 30px;
  }

  &__footer-bottom {
    padding: 25px 0;
  }
}
.footer-top {
  background-color: #17213c;
  &__container {
    display: flex;
    padding: 0 -15px;
  }

  &__column {
    padding: 0 15px;
  }

  @media (max-width: 484px) and (min-width: 342px) {
    &__column {
      flex: 0 1 50%;
    }
  }

  @media (max-width: 704px) {
    &__container {
      flex-wrap: wrap;
    }

    &__column {
      padding-top: 20px;
    }
  }

  &__label {
    margin-bottom: 20px;

    font-weight: 700;
    font-size: 16px;
    line-height: 150%;
    letter-spacing: 0.1px;
    color: #ffffff;
  }

  &__menu-footer {
  }
}
.menu-footer {
  &__list {
    > *:not(:last-child) {
      padding-bottom: 10px;
    }
  }

  &__item {
    display: flex;
    align-items: center;

    font-weight: 600;
    font-size: 14px;
    line-height: 171%;
    letter-spacing: 0.2px;
    color: #ffffff;
  }

  &__item:hover {
    text-decoration-line: underline;
  }

  &__link {
    display: flex;
    align-items: center;
    > *:not(:last-child) {
      padding-right: 10px;
    }
  }

  &__icon {
  }
}
.footer-bottom {
  &__container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    padding-right: 40px;
  }

  &__made-by {
    font-weight: 600;
    font-size: 14px;
    line-height: 171%;
    letter-spacing: 0.2px;
    color: #737373;

    margin-right: 30px;
  }

  &__socials {
    display: flex;
    align-items: center;

    > *:not(:last-child) {
      margin-right: 20px;
    }
  }

  @media (max-width: 582px) {
    &__socials {
      margin-top: 10px;
    }
  }

  &__img {
  }
}
</style>