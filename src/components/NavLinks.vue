<template>
    <li class="text-center mb-3">
        <a href="">{{ link }}</a>
    </li>
</template>

<script>
export default {
    name: 'NavLinks',
    props: ['link']
}
</script>

<style lang="scss" scoped>
a {
    text-decoration: none;
    color: white;

    &:hover {
        color: var(--primary-color);
    }
}
</style>