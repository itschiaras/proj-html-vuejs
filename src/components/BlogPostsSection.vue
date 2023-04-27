<template>
    <div class="ms-container mx-auto">
        <div id="triangle">
        </div>
        <div class="text-center mb-5">
            <p class="text-uppercase m-0">tales from the barbershop</p>
            <h2>Recent Blog Posts</h2>
        </div>
        <div class="container mb-5">
            <div class="row row-cols-3">
                <div class="col text-center" v-for="post in posts">
                    <img :src="getImagePath(`../assets/images/${post.src}`)" alt="">
                    <h3 class="mb-4 mt-4">{{ post.title }}</h3>
                    <span class="fw-light">{{ post.text }}</span>
                </div>
            </div>
        </div>
        <div class="d-flex justify-content-center">
            <CustomizedButton :text="'read more from our blog'"/>
        </div>
        
    </div>
</template>

<script>
import { posts } from '../assets/store/store';
import CustomizedButton from './CustomizedButton.vue';
export default {
    name: "BlogPostsSection",
    data() {
        return {
            posts: [...posts]
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
#triangle {
    background-image: url(../assets/images/triangle.svg);
    height: 60px;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    transform: rotate(180deg);
}

p {
    color: var(--primary-color);
    font-weight: bold;
}

img {
    width: 300px;
}
</style>