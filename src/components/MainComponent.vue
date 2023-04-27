<template>
    <main>
        <section id="ourTeam">
            <OurTeamSection />
        </section>
        <section id="services">
            <ServicesSection />
        </section>
        <section id="shop">
            <ShopSection />
        </section>
        <section id="reviews">
            <ReviewsSection />
        </section>
        <section id="blogPosts">
            <BlogPostsSection />
        </section>
    </main>
</template>

<script>
import OurTeamSection from '../components/OurTeamSection.vue'
import ServicesSection from '../components/ServicesSection.vue'
import ShopSection from '../components/ShopSection.vue'
import ReviewsSection from '../components/ReviewsSection.vue'
import BlogPostsSection from '../components/BlogPostsSection.vue'

export default {
    name: 'MainComponent',
    components: { OurTeamSection, ServicesSection, ShopSection, ReviewsSection, BlogPostsSection }
}
</script>

<style lang="scss" scoped>
#ourTeam {
    background-image: url(../assets/images/avadabarbers-about-introbackground.jpg);
    background-size: cover;
    height: 400px;
    position: relative;
}

#services {
    height: 650px;
    position: relative;
}

#shop {
    background-image: url(../assets/images/avadabarbers-reviewsbackground.jpg);
    background-size: cover;
    height: 800px;
    position: relative;
}

#blogPosts {
    background-color: #f5f5f5;
}

#reviews {
    padding-top: 25rem;
    padding-bottom: 5rem;
}
</style>