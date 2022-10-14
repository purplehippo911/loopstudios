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
                        <div class="container row">
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
                </div>
            </section>
            
            <section class="gallery-section">
                <div class="container gallery">
                    <h2 class="gallery__title"> Our creations</h2>
                    
                    <div class="gallery__item deep-earth">
                            <h3 class="gallery__info">Deep earth</h3>
                            <div class="gallery__wrapper"></div>
                    </div>

                    <div class="gallery__item night-arcade">
                        <h3 class="gallery__info">Night arcade</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <div class="gallery__item soccer-team">
                        <h3 class="gallery__info">Soccer team VR</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <div class="gallery__item the-grid">
                        <h3 class="gallery__info">The grid</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <div class="gallery__item from-above">
                        <h3 class="gallery__info">From up above VR</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <div class="gallery__item pocket-borealis">
                        <h3 class="gallery__info">Pocket borealis</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <div class="gallery__item curiosity">
                        <h3 class="gallery__info">The curiosity</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <div class="gallery__item fisheye">
                        <h3 class="gallery__info">Make it fisheye</h3>
                        <div class="gallery__wrapper"></div>
                    </div>
                    
                    <button class="gallery__button"> See all </button>
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
  @import '../styles/variables.scss';
  @import '../styles/mixin.scss';

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
        position:relative;
    
        .grid {
            grid-template-columns: repeat(auto-fill, minmax(500px, 1fr));
            @media screen and (min-width:800px) {
                @include grid(2, 600px, 2fr);
                justify-content: center;
            }
        }
    }

    .interactive__col {
        box-shadow: 2px 0px 10px 0px $DarkGray;
        .container {
            padding:5rem;
        }
        @media screen and (min-width:800px) {
            position: absolute;
            background: white;
            bottom: 10px;
            right: 150px;
            width: 50%;
        }
    }

    .gallery {
        @include grid(auto-fill, 200px, 1fr);
        gap:2rem;
        text-align:unset;
        .gallery__title {
            grid-column:1 / -1;
            align-self:center;
            justify-self: center;
            @media screen and (min-width:800px) {
                justify-self: start;
                grid-column:1 / 3;

             }
        }

        .gallery__item {
            width: 100%;
            height:10rem;
            padding:2rem;
            position:relative;
            color:$White;
            text-align: left;
            display: flex;
            align-items: flex-end;
            font-size: 1.21em;
            @media screen and (min-width:800px) {
                height: 20rem;
            }
            &:hover {
                color:$Black;
            }
            .gallery__wrapper {
                background: $White;
                position: absolute;
                bottom: 0;
                left: 0px;
                width: 100%;
                height: .2vh;
                opacity: .5;
                transition:0.5s ease-out;
            }
        }
        .gallery__item:hover .gallery__wrapper {
            height:100%;
        }
        .deep-earth {
            @include backgroundIMG("../assets/images/mobile/image-deep-earth.jpg", "../assets/images/desktop/image-deep-earth.jpg");
            &:hover {
                color:$White;
            }
        }

        .night-arcade {
            @include backgroundIMG("../assets/images/mobile/image-night-arcade.jpg", "../assets/images/desktop/image-night-arcade.jpg");
        }

        .soccer-team {
            @include backgroundIMG("../assets/images/mobile/image-soccer-team.jpg", "../assets/images/desktop/image-soccer-team.jpg");
        }

        .the-grid {
            @include backgroundIMG("../assets/images/mobile/image-grid.jpg", "../assets/images/desktop/image-grid.jpg");
        }
        
        .from-above {
            @include backgroundIMG("../assets/images/mobile/image-from-above.jpg", "../assets/images/desktop/image-from-above.jpg");
        }
        .pocket-borealis {
            @include backgroundIMG("../assets/images/mobile/image-pocket-borealis.jpg", "../assets/images/desktop/image-pocket-borealis.jpg");
        }
        .curiosity {
            @include backgroundIMG("../assets/images/mobile/image-curiosity.jpg", "../assets/images/desktop/image-curiosity.jpg");
        }
        .fisheye {
            @include backgroundIMG("../assets/images/mobile/image-fisheye.jpg", "../assets/images/desktop/image-fisheye.jpg");
        }
        
        .gallery__button {
            border:0;
            padding:.5rem 1.5rem;
            font-family:$Alata;
            text-transform:uppercase;
            border:2px solid $Black;
            background:$White;
            color:$Black;

            grid-row-start: 10;
            justify-self: center;
            align-self:center;
            grid-column:1 / -1;
            transition:0.5s ease-in-out;

            @media screen and (min-width:800px) {
                grid-row-start: 1;
                grid-column: 3/-1;
                justify-self: end;
             }

            &:hover {
                background:$Black;
                color:$White;
            }
        }
    }

</style> 