<template>
    <header>
        
        <div class="ms-container mx-auto">
            <nav class="d-flex align-items-center justify-content-between">
                <img src="../assets/images/avadabarbers-logo-x1.png" alt="">
                <div>
                    <a href=""><i class="fa-solid fa-cart-shopping"></i></a>
                    <a href=""><i class="fa-solid fa-bars"></i></a>
                    
                </div>
            </nav>
            <div class="d-flex">
                <div class="w-50 d-flex flex-column justify-content-center align-items-start">
                    <h1>Barber Shop</h1>
                    <hr class="w-50">
                    <p>The Pinnacole of Male Grooming</p>
                    <CustomizedButton :text="'learn more'"/>
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
export default {
    name: 'HeaderComponent',
    components: {CustomizedButton}
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
}
</style>