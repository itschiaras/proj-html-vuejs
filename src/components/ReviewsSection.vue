<template>
    <div class="ms-container mx-auto">
        <div class="text-center">
            <p class="text-uppercase m-0">what people say</p>
            <h2 class="mb-5">Reviews</h2>
            <div class="container">
                <div class="row gap-5">
                    <div class="col text-center" v-for="review in reviews">
                        <p>{{ review.text }}</p>
                        <img :src="getImagePath(`../assets/images/${review.src}`)" alt="" class="mb-3">
                        <span class="d-block">{{ review.name }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { reviews } from '../assets/store/store';
export default {
    name: 'ReviewsSection',
    data() {
        return {
            reviews: [...reviews]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>
p {
    color: var(--primary-color);
    font-weight: bold;
}

.container {
    p {
        color: #525252;
        font-weight: 300;
    }
    img {
        border-radius: 50%;
        width: 100px;
    }
    span {
        font-style: italic;
        color: var(--primary-color);
        font-weight: bold;
    }
}
</style>