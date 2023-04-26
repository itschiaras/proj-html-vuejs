<template>
    <a href="" class="text-uppercase">
        <span>{{ text }}</span>
    </a>
</template>

<script>
    export default {
        name: 'CustomizedButton',
        props: ['text']
    }
</script>

<style lang="scss" scoped>
a {
    border: 1px solid var(--primary-color);
    text-decoration: none;
    color: var(--primary-color);
    padding: .8rem 2rem;
    transition: .5s all;
    &:hover {
        color: #855f2d;
        border-color: #855f2d;
    }
}
</style>