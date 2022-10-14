<template>
    <footer>
        <div class="container grid">
            
            <a href="#" class="logo">
                <img src="../assets/images/logo.svg" alt="our logo">
            </a>

            <ul class="footer__list">
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        About
                    </a>
                </li>
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        Careers
                    </a>
                </li>
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        Events
                    </a>
                </li>
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        Products
                    </a>
                </li>
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        Support
                    </a>
                </li>
            </ul>

            <ul class="footer__socials">
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        <img src="../assets/images/icon-facebook.svg" alt="Facebook icon. Follow us on Facebook.">
                    </a>
                </li>
                <li class="footer__item">
                    <a href="#" class="footer__link">
                        <img src="../assets/images/icon-twitter.svg" alt="Twitter icon. Follow us on Twitter.">
                    </a>
                </li>
                <li class="footer__item">
                    <a href="" class="footer__link">
                        <img src="../assets/images/icon-pinterest.svg" alt="Pinterest icon. Follow us on Pinterest">
                    </a>
                </li>
                <li class="footer__item">
                    <a href="" class="footer__link">
                        <img src="../assets/images/icon-instagram.svg" alt="Instagram icon. Follow us on Instagram">
                    </a>
                </li>
            </ul>

            <p class="footer__info">© 2021 Loopstudios. All rights reserved.</p>
            
        </div>
    </footer>


  <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
    Coded by <a href="https://www.frontendmentor.io/profile/purplehippo911">Purplehippo911</a>.
  </div>

</template>

<script>
export default {
    name: 'FooterPart',
    data() {
        return {
        }
    }
    }
</script>

<style lang="scss">
@import '../styles/variables.scss';
@import '../styles/mixin.scss';

footer {
    background:$Black;
    padding:2rem;
    text-align:center;
    .grid {
      display:flex;
      flex-direction:column;
      @media screen and (min-width:800px) {
          display:grid;
          justify-items: start;
          grid-template-areas:
          "🎈 🎈 📱 📱 📱"
        "✉ ✉ ✉ 🧾 🧾";
        align-items: center;
      }
    }
    .logo {
        grid-area:🎈;
    }
    .footer__list {
    display: flex;
    flex-direction:column;
    list-style: none;
    grid-area:✉;
    @media screen and (min-width:800px) {
        flex-direction:row;
    }
  }

  .footer__item:hover .footer__link::after {
    content:"";
    width: 100%;
    padding: 0.1rem;
    background:$White;
    margin-top: 0.3rem;
  }

  .footer__link {
    margin: 2rem;
    text: {
        decoration: none;
        transform:uppercase;
    }
    color: $White;
    font-family:'Alata', sans-serif;
    display: flex;
    flex-direction: column;
  }
  .footer__socials {
      display:flex;
      grid-area: 📱;
  }
  .footer__info {
    grid-area:🧾;
    margin-top:0;
  }

  .footer__socials, .footer__info {
    justify-self:end;
  }

}

.attribution { 
    font-size: 20px;
    margin: 2rem 0;
    text-align: center;
    .attribution a { 
        color: hsl(228, 45%, 44%); 
    }
}
</style> 