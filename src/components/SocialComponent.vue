<template>
    <li>
        <a href="">
            <i :class="`${icon}`"></i>
        </a>
    </li>
</template>

<script>
    export default {
        name: 'SocialComponent',
        props: ['icon']
    }
</script>

<style lang="scss" scoped>
a {
    text-decoration: none;
    color: var(--secondary-color);
    &:hover {
        color: white;
    }
}
</style>