<template>
    <main>
        <div class="container row">
            <section class="interactive-section">
                <div class="container grid">
                    <picture>
                        <source media="(min-width:770px)" srcset="../assets/images/desktop/image-interactive.jpg">
                        <source media="(max-width:665px)" srcset="../assets/images/mobile/image-interactive.jpg">
                        <img src="../assets/images/mobile/image-interactive.jpg" alt="someone playing a VR game">
                    </picture>

                    <div class="interactive__col">
                        <h2 class="interactive__title">
                            The leader in interactive VR
                        </h2>
                        <p class="interactive__info">
                            Founded in 2011, Loopstudios has been producing world-class virtual reality
                            projects for some of the best companies around the globe. Our award-winning
                            creations have transformed businesses through digital experiences that bind
                            to their brand.
                        </p>
                    </div>
                </div>
            </section>
            
            <section class="gallery-section">
                <div class="container gallery">
                    <h2 class="gallery__title"> Our creations</h2>
                    
                        <div class="gallery__item deep-earth">
                            <p class="gallery__info">Deep earth</p>
                        </div>
                        <div class="gallery__item night-arcade">
                            <p class="gallery__info">Night arcade</p>
                        </div>
                        <div class="gallery__item soccer-team">
                            <p class="gallery__info">Soccer team VR</p>
                        </div>
                        <div class="gallery__item the-grid">
                            <p class="gallery__info">The grid</p>
                        </div>
                        <div class="gallery__item from-above">
                            <p class="gallery__info">From up above VR</p>
                        </div>
                        <div class="gallery__item pocket-borealis">
                            <p class="gallery__info">Pocket borealis</p>
                        </div>
                        <div class="gallery__item curiosity">
                            <p class="gallery__info">The curiosity</p>
                        </div>
                        <div class="gallery__item fisheye">
                            <p class="gallery__info">Make it fisheye</p>
                        </div>

                    <button class="gallery_button"> See all </button>
                </div>
            </section>
        </div>
    </main>
</template>

<script>
export default {
    name: 'MainPart',
    data() {
        return {
        }
    }
    }
</script>

<style lang="scss" scoped>
  @import '../variables.scss';

  @mixin backgroundIMG($Mobile, $Desktop) {
        background:url($Mobile) no-repeat;
        background-size:cover;
        @media screen and (min-width:800px) {
            background:url($Desktop) no-repeat;
         }
    }

    main {
        margin: 2rem 0;
    }

    .container {
        width:100%;
    }

    .row {
        flex-direction:column;
    }

    section {
        width:80%;
        padding:5rem;
        text-align:center;
        .grid {
            @media screen and (min-width:800px) {
                display: grid;
                justify-items: center;
                grid-template-columns: repeat(auto-fit, minmax(200px, 2fr));
            }
        }
    }


    picture, .interactive__col {
        width:100%
    }

    .interactive__col {
        @media screen and (min-width:800px) {
            position:aboslute;
        }
    }

    .gallery {
        display:grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        .gallery__title {
            grid-column:1 / -1;
        }
        .gallery__item {
            width:100%;
            padding:2rem;
        }

        .deep-earth {
            @include backgroundIMG('../assets/images/mobile/image-deep-earth.jpg', '../assets/images/desktop/image-deep-earth.jpg');
            // background:url('../assets/images/mobile/image-deep-earth.jpg') no-repeat;
            // background-size:cover;
            // @media screen and (min-width:800px) {
            //     background:url('../assets/images/desktop/image-deep-earth.jpg') no-repeat;
            //  }
            }
        
        
        

    }

</style> 