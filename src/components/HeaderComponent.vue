<template>
    <header>

        <div class="ms-container mx-auto">
            <nav class="d-flex align-items-center justify-content-between">
                <img src="../assets/images/avadabarbers-logo-x1.png" alt="">
                <div>
                    <a href=""><i class="fa-solid fa-cart-shopping"></i></a>
                    <a data-bs-toggle="offcanvas" href="#offcanvasExample" role="button" aria-controls="offcanvasExample">
                        <i class="fa-solid fa-bars"></i>
                    </a>

                    <div class="offcanvas offcanvas-end w-100 " tabindex="-1" id="offcanvasExample"
                        aria-labelledby="offcanvasExampleLabel">
                        <div class="offcanvas-header">
                            <button type="button" class="btn-close-white ms-auto" data-bs-dismiss="offcanvas"
                                aria-label="Close" id="closeBtn">X</button>
                        </div>
                        <div class="offcanvas-body d-flex justify-content-center align-items-center">
                            <ul class="list-unstyled">
                                <li v-for="link in headerLinks" class="mb-3">
                                    <a href="">{{ link.text }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>

                </div>
            </nav>
            <div class="d-flex">
                <div class="w-50 d-flex flex-column justify-content-center align-items-start">
                    <h1>Barber Shop</h1>
                    <hr class="w-50">
                    <p>The Pinnacole of Male Grooming</p>
                    <CustomizedButton :text="'learn more'" />
                </div>
                <div class="w-50 text-center">
                    <img src="../assets/images/avadabarbers_hero_focalmirror-400x550.png" alt="">
                </div>
            </div>
        </div>

    </header>
</template>

<script>
import CustomizedButton from '../components/CustomizedButton.vue'
import { headerLinks } from '../assets/store/store'
export default {
    name: 'HeaderComponent',
    components: { CustomizedButton },
    data() {
        return {
            headerLinks: [...headerLinks]
        }
    }
}
</script>

<style lang="scss" scoped>
header {
    background-image: url(../assets/images/avadabarbers-homepage-hero-bg.jpg);
    background-size: cover;
    color: white;
    height: 750px;

    nav {
        height: 90px;
    }

    i {
        color: white;
        margin-right: 1rem;
    }

    h1 {
        font-family: 'Abril Fatface', cursive;
        font-size: 5rem;
    }

    hr {
        border-top: .3rem solid;
        color: var(--primary-color);
        opacity: 1;
    }

    p {
        color: #b0b0b0;
        font-weight: 300;
        font-size: 1.4rem
    }

    #closeBtn {
        border: 0;
        background-color: transparent;
        font-weight: bold;
    }

    .offcanvas {
        background-color: #121212;
    }

    a {
        text-decoration: none;
        color: white;
        &:hover {
            color: var(--primary-color);
        }
    }
}
</style>