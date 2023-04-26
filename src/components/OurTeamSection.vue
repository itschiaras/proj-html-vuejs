<template>
    <div class="ms-container mx-auto d-flex justify-content-center align-items-center h-75">
        <div class="text-center">
            <p class="text-uppercase m-0">award winning</p>
            <h2 class="mb-4">Pro Barbers</h2>
            <CustomizedButton :text="'meet your new barber'" />
        </div>
    </div>
    <div id="triangle">
    </div>
</template>

<script>
import CustomizedButton from './CustomizedButton.vue';
export default {
    name: 'OurTeamSection',
    components: { CustomizedButton }
}
</script>

<style lang="scss" scoped>

p {
    color: var(--primary-color);
    letter-spacing: .2rem;
}

#triangle {
    background-image: url(../assets/images/triangle.svg);
    height: 60px;
    width: 100%;
    position: absolute;
    bottom: 0;
}
</style>