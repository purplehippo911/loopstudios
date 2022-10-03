<template>
  <header>
    <div class="container grid">
      <a class="logo" href="#">
        <img src="../assets/images/logo.svg" alt="our logo">
      </a>

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

        <div class="dropdown container grid" ref="dropdown">
  
          <a class="logo" href="#">
          <img src="../assets/images/logo.svg" alt="our logo">
        </a>
        
        <a class="header__icons" href="#" @click="toggleNav">
            <img src="../assets/images/icon-hamburger.svg" alt="hamburger" ref="hamburger" />
            <img src="../assets/images/icon-close.svg" alt="close" class="close" ref="closeButton"/>
        </a>

          <nav class="dropdown__nav">
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

      <a class="header__icons" href="#" @click="toggleNav">
        <img src="../assets/images/icon-hamburger.svg" alt="hamburger" ref="hamburger" />
        <img src="../assets/images/icon-close.svg" alt="close" class="close" ref="closeButton"/>
      </a>

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
  },

  methods: {
    toggleNav() {
      this.$refs.hamburger.classList.toggle('close');
      this.$refs.closeButton.classList.toggle('close');
      this.$refs.dropdown.classList.toggle('close');
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

.grid {
  display:grid;
  align-items: center;
  grid-template-columns: 3fr 2fr;
  gap: 3rem;
}

.logo {
  margin-right:auto;
}

.nav {
  width:50%;
  display:none;
  .nav__list {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
  
  .nav__link {
    text-decoration: none;
    color: $White;
  }
  @media screen and (min-width:800px) {
    display:flex;
  }

}

.dropdown {
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  background:$Black;
  .dropdown__nav {
    @extend .nav;
    display:flex;
  }
}

.dropdown.container {
  width:100%;
}


.header__icons {
  justify-self:end;
  width:3rem;
  &:focus ~ nav {
    display:flex;
  }
}


.header__hero {
  font-size: 2.7em;
  border: 2px solid $White;
  color:$White;
  align-self: center;
}

.header__title {
  text-transform: uppercase;
  width: 57%;
  padding: 2rem;
}
</style>
  