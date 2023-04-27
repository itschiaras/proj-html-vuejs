<template>
    <footer>
        <div class="d-flex align-items-center" id="footer-top">
            <div class="ms-container mx-auto">
                <div class="container">
                    <div class="row gap-4">
                        <div class="col d-flex flex-column align-items-center">
                            <img src="../assets/images/avadabarbers_footer_shop_image-300x234.png" alt="" class="mb-4">
                            <CustomizedButton :text="'shop our range now'" />
                        </div>
                        <div class="col d-flex flex-column align-items-center justify-content-between">
                            <img src="../assets/images/avadabarbers-logo-x2-200x70.png" alt="">
                            <p class="text-center fw-light">
                                Avada Barbers
                                <br>
                                123 New York Street
                                <br>
                                New York City
                                <br>
                                info@yourwebsite.com
                                <br>
                                +1 (555) 555-1212
                            </p>
                            <p class="follow text-uppercase m-0">follow us</p>
                            <div class="d-flex social-list">
                                <ul class="list-unstyled d-flex gap-2 w-50">
                                    <SocialComponent :icon="social.icon" v-for="social in socials"/>
                                </ul>
                            </div>
                        </div>
                        <div class="col d-flex flex-column align-items-center">
                            <img src="../assets/images/avadabarbers_footer_appointment_image-300x234.png" alt=""
                                class="mb-4">
                            <CustomizedButton :text="'book your appointment'" />
                        </div>
                    </div>
                </div>
            </div>

        </div>
        <div id="footer-bottom" class="d-flex align-items-center">
            <div class="ms-container mx-auto text-center">
                <p class="m-0">Coded with &hearts; by Chiara</p>
            </div>

        </div>
    </footer>
</template>

<script>
import CustomizedButton from './CustomizedButton.vue';
import SocialComponent from './SocialComponent.vue';
import { socials } from '../assets/store/store';

export default {
    name: "FooterComponent",
    components: { CustomizedButton, SocialComponent },
    data() {
        return {
            socials: [...socials]
        }
    }
}
</script>

<style lang="scss" scoped>
footer {
    color: white;

    #footer-top {
        background-color: #121314;
        height: 400px;
    }

    #footer-bottom {
        background-color: #161718;
        height: 100px;
        p {
            word-spacing: .3rem;
            color: var(--secondary-color);
            font-weight: 300;
            font-size: .8rem;
        }
    }

    p {
        color: var(--secondary-color);
    }

    .follow {
        color: var(--primary-color);
        font-weight: bold;
    }

    ul {
        width: 30px;
        margin-bottom: 0;
        color: var(--secondary-color);
    }
}
</style>