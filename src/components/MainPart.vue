<template>
    <main>
        <div class="container row">
            <section class="interactive-section">
                <div class="container row">
                    <picture>
                        <source media="(min-width:770px)" srcset="../assets/images/desktop/image-interactive.jpg">
                        <source media="(max-width:665px)" srcset="../assets/images/mobile/image-interactive.jpg">
                        <img src="../assets/images/mobile/image-interactive.jpg" alt="someone playing a VR game">
                    </picture>

                    <div class="interactive__col">
                        <h1 class="interactive__title">
                            The leader in interactive VR
                        </h1>
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
                <div class="container grid">
                    <h1 class="gallery_title"> Our creations</h1>
                    
                        <div class="gallery__item">
                            <p class="gallery__info">Deep earth</p>
                        </div>
                        <div class="gallery__item">
                            <p class="gallery__info">Night arcade</p>
                        </div>
                        <div class="gallery__item">
                            <p class="gallery__info">Soccer team VR</p>
                        </div>
                        <div class="gallery__item">
                            <p class="gallery__info">The grid</p>
                        </div>
                        <div class="gallery__item">
                            <p class="gallery__info">From up above VR</p>
                        </div>
                        <div class="gallery__item">
                            <p class="gallery__info">Pocket borealis</p>
                        </div>
                        <div class="gallery__item">
                            <p class="gallery__info">The curiosity</p>
                        </div>
                        <div class="gallery__item">
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

<style lang="scss">
    @import '../_variables';

    main {
        margin: 2rem;
        padding: 2rem;
    }

    section {
        width:80%;

    }


</style> 