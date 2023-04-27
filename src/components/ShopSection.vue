<template>
    <div class="container mx-auto pt-6">
        <div class="d-flex flex-column h-100 justify-content-evenly">
            <div class="text-center">
                <p class="text-uppercase m-0">we have you covered</p>
                <h2>Avada Grooming Products</h2>
            </div>
        </div>
        <div class="container">
            <div class="row row-cols-4">
                <div class="col text-center" v-for="product in products">
                    <img :src="getImagePath(`../assets/images/${product.src}`)" alt="" class="img-fluid">
                    <h3 class="mb-4 mt-4">{{ product.name }}</h3>
                    <span>{{ product.price }}</span>
                </div>
            </div>
            <div class="text-center mt-5 mb-6">
                <CustomizedButton :text="'shop our product range'" />
            </div>
        </div>
        <div id="specialProduct" class="position-absolute">
            <div class="container w-100 h-100 p-0">
                <div class="row w-100 h-100 p-0 m-0">
                    <div class="col-5 bg-shop d-flex align-items-center">
                        <img src="../assets/images/shaving_butter-600x600.png" alt="" class="img-fluid">
                    </div>
                    <div class="col p-5 d-flex align-items-center">
                        <div>
                            <p class="text-uppercase m-0">this month featured product</p>
                            <h2>Shaving butter</h2>
                            <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque laoreet enim est, vel molestie dolor ultrices ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span>
                            <div class="mt-5">
                                <CustomizedButton :text="'buy now'"/>
                            </div>
                            
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { products } from '../assets/store/store';
import CustomizedButton from './CustomizedButton.vue';
export default {
    name: 'ShopSection',
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
    data() {
        return {
            products: [...products]
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

span {
    color: var(--primary-color);
}

.pt-6 {
    padding-top: 4rem;
}

#specialProduct {
    height: 350px;
    width: 60%;
    bottom: -300px;
    left: 20%;
    background-color: #121413;
    border-top: 3px solid var(--primary-color);
    span {
        color: var(--secondary-color);
        font-weight: 300;
    }
}

.bg-shop {
    background-image: url(../assets/images/avadabarbers-cta-background.jpg);
    background-size: cover;
    height: 100%;
}
</style>