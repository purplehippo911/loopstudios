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
            <img src="../assets/images/icon-close.svg" alt="close" class="closeButton" ref="dropdownClose"/>
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
        <img src="../assets/images/icon-hamburger.svg" alt="hamburger" class="hamburger" ref="hamburger" />
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

      
      this.$refs.dropdownClose.classList.toggle('open');
      this.$refs.dropdownClose.classList.toggle('active');

      
      this.$refs.dropdown.classList.toggle('open');
      this.$refs.dropdown.classList.toggle('active');
    }
  }
}

</script>
  
<style lang="scss">
@import '../_variables';



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
  width:100%;
  padding:2rem,
}

.nav {
  width:100%;
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
  display:none;
  opacity:0;
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  background:$Black;
  transition:0.7s ease-in-out;
  .dropdown__nav {
    @extend .nav;
    display:flex;
    width: 100%;
    .row {
    justify-content:flex-end;
    }
    .nav__list {
      flex-direction:column;
    }
  }
}


.header__icons {
  justify-self:end;
  width:3rem;
  &:focus ~ nav {
    display:flex;
  }
}

.closeButton {
  display:none;
  opacity:0;
  transition:0.7s ease-in-out;
}

.hamburger {
  transition:0.7s ease-in-out;
  @media screen and (min-width:800px) {
    display:none;
  }
}

.header__hero {
  font-size: 2.7em;
  border: 2px solid $White;
  color:$White;
  grid-row-start: 2;
}

.header__title {
  text-transform: uppercase;
  width: 57%;
  padding: 2rem;
}

.close {
  display:none;
}

.open {
  display:grid;
}

.active {
  opacity:1;
}

</style>
  