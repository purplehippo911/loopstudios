<template>
    <footer>
        <div class="container row">
            
            <ul class="footer__list">
                <li class="footer__item">About</li>
                <li class="footer__item">Careers</li>
                <li class="footer__item">Events</li>
                <li class="footer__item">Products</li>
                <li class="footer__item">Support</li>
            </ul>
            
            <ul class="footer__socials li footer__item">
                <img src="../assets/images/icon-facebook.svg" alt="Facebook icon. Follow us on Facebook.">
            </ul>
            <ul class="footer__socials li footer__item">
                <img src="../assets/images/icon-twitter.svg" alt="Twitter icon. Follow us on Twitter.">
            </ul>
            <ul class="footer__socials li footer__item">
                <img src="../assets/images/icon-pinterest.svg" alt="Pinterest icon. Follow us on Pinterest">
            </ul>
            <ul class="footer__socials li footer__item">
                <img src="../assets/images/icon-instagram.svg" alt="Instagram icon. Follow us on Instagram">
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
@import '../variables.scss';

.attribution { font-size: 11px; text-align: center; }
    .attribution a { color: hsl(228, 45%, 44%); }
</style> 