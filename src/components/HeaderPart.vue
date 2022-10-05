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
  
<style lang="scss" scoped>
@import '../_variables.scss';



header {
  background: url("../assets/images/desktop/image-hero.jpg") no-repeat;
  background-size: cover;

  @media screen and (min-width:800px) {
    background: url("../assets/images/desktop/image-hero.jpg") no-repeat;
  }

}

.grid {
  display:grid;
  align-items: center;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}

.logo {
  padding:2rem;
  text-align: center;
  @media screen and (min-width:800px) {
    grid-column: span 2;
  }
}

.nav {
  width:80%;
  display:none;
  grid-column: span 3;
  justify-self: end;
  .nav__list {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
  
  .nav__link {
    text-decoration: none;
    color: $DarkGray;
    font-size:2.2em;
    text-transform:uppercase;
    font-family:'Alata', sans-serif;
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
  grid-template-columns: repeat(auto-fit, minmax(169px, 1fr));
  @media screen and (min-width:800px) {
    display:none;
    opacity:0;
  }
  .dropdown__nav {
    @extend .nav;
    display:flex;
    grid-column:span 1;
    grid-row-start: 2;
    justify-self: start;
    .nav__list {
      flex-direction:column;
    }
    .header__icons {
      grid-row-start: 3;
    }
  }
}


.header__icons {
  width:3rem;
  justify-self: end;
  text-align:center;
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
  grid-column: span 2;
  @media screen and (min-width:800px) {
    grid-column: span 3;
  }
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
  