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
    </div>

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
      Immersive experiences that deliver
    </div>
  </header>
    <p> {{ message }}</p>
  </template>
  
  <script>
  
  export default {
    name: 'HeaderPart',
    data() {
        return {
            message: 'this finally works, right'
        }
    }
    }
  
  </script>
  
  <style lang="scss">
  @import '../_variables';

  header {
    width:100%;
    padding:1rem;
    background: url("../assets/images/desktop/image-hero.jpg") no-repeat;
    background-size:cover;
    @media screen and (min-width:800px) {
      background: url("../assets/images/desktop/image-hero.jpg") no-repeat;
    }
  }

  .nav__list {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .nav__link {
    text-decoration:none;
    color:$White;
  }

  .close {
    display:none;
  }
  
  </style>
  