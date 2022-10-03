<template>
  <header>
    <div class="container row">
      <a class="logo" href="#">
        <img src="../assets/images/logo.svg" alt="our logo">
      </a>

      <nav class="nav close">
        <div class="container row">
          <ul class="nav__list">
            <li class="nav__item">
              <a href="#" class="nav__link">
                About
              </a>
            </li>
            <li class="nav__item">
              <a href="#" class="nav__link">
                Careers
              </a>
            </li>
            <li class="nav__item">
              <a href="#" class="nav__link">
                Events
              </a>
            </li>
            <li class="nav__item">
              <a href="#" class="nav__link">
                Products
              </a>
            </li>
            <li class="nav__item">
              <a href="#" class="nav__link">
                Support
              </a>
            </li>
          </ul>
        </div>
      </nav>

      <a class="header__icons" href="#">
        <img src="../assets/images/icon-hamburger.svg" alt="hamburger" />
        <img src="../assets/images/icon-close.svg" alt="close" class="close" />
      </a>
      <div class="dropdown close">

        <nav class="nav">
          <div class="container row">
            <ul class="nav__list">
              <li class="nav__item">
                <a href="#" class="nav__link">
                  About
                </a>
              </li>
              <li class="nav__item">
                <a href="#" class="nav__link">
                  Careers
                </a>
              </li>
              <li class="nav__item">
                <a href="#" class="nav__link">
                  Events
                </a>
              </li>
              <li class="nav__item">
                <a href="#" class="nav__link">
                  Products
                </a>
              </li>
              <li class="nav__item">
                <a href="#" class="nav__link">
                  Support
                </a>
              </li>
            </ul>
          </div>
        </nav>
      </div>

      <div class="header__hero">
        <h2 class="header__title">Immersive experiences that deliver</h2>
      </div>
    </div>

  </header>
</template>
  
<script>

export default {
  name: 'HeaderPart',
  data() {
    return {
    }
  }
}

</script>
  
<style lang="scss">
@import '../_variables';

.close {
  display: none;
}

header {
  width: 100%;
  padding: 3rem 0;
  background: url("../assets/images/desktop/image-hero.jpg") no-repeat;
  background-size: cover;

  @media screen and (min-width:800px) {
    background: url("../assets/images/desktop/image-hero.jpg") no-repeat;
  }
}

.logo {
  margin-right:auto;
}

.nav__list {
  display: flex;
  gap: 2rem;
  list-style: none;
}

.nav__link {
  text-decoration: none;
  color: $White;
}

.header__hero {
  // padding:2rem;
  font-size: 2em;
  border: 2px solid $White;
  align-self: center;
}

.header__title {
  text-transform: uppercase;
  width: 50%;
}
</style>
  