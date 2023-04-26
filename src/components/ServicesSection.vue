<template>
    <div class="ms-container mx-auto h-100">
        <div class="d-flex flex-column h-100 justify-content-evenly">
            <div class="text-center">
                <p class="text-uppercase m-0">mens grooming</p>
                <h2>Services</h2>
            </div>
            <div class="container">
                <div class="row gap-5">
                    <div class="col text-center" v-for="service in services">
                        <img :src="getImagePath(`../assets/images/${service.src}`)" alt="">
                        <h3 class="mb-4 mt-4">{{ service.title }}</h3>
                        <span>{{ service.text }}</span>
                    </div>
                </div>
                <div class="text-center mt-5 mb-6">
                <CustomizedButton :text="'read about our services'" />

            </div>
            </div>
            
            

        </div>
        <div id="triangle">
            </div>



    </div>
</template>

<script>
import { services } from '../assets/store/store.js'
import CustomizedButton from './CustomizedButton.vue';
export default {
    name: "ServicesSection",
    data() {
        return {
            services: [...services]
        };
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
    components: { CustomizedButton }
}
</script>

<style lang="scss" scoped>
p {
    color: var(--primary-color);
    font-weight: bold;
}

img {
    width: 55px;
    height: 80px;
}

span {
    font-weight: 300;
}

#triangle {
    background-image: url(../assets/images/triangle.svg);
    height: 60px;
    width: 100%;
    position: absolute;
    bottom: 0;
    left:0;
    filter: invert(100%);
}

.mb-6 {
    margin-bottom: 7rem;
}
</style>