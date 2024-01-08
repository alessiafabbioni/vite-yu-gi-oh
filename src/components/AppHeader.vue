<script>
export default {
    name: 'AppHeader',
    props: ['message']

}


</script>

<template>
    <header class="container">
        <img src="/public/img/logo.jpeg" alt="Yughi logo">
        <h1>{{ message }}</h1>

    </header>


</template>

<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

header{
    background-color: $secondary-bg-color;
    max-height: 60px;
    display: flex;
    flex-direction: row;
    margin: 2rem;

    img {
        height: 100%;
        width: 10%;
        object-fit: cover;
        padding-right: 1rem;
    }
}


</style>