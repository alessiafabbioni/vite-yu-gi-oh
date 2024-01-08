<script>
export default {
    name: 'SingleCharacter',
    props: {
        info: Object
    }

}


</script>

<template>
<div class="character text-center">
    <img class="img-fluid mb-3" :src="info.card_images[0].image_url" :alt="info.name">
    <h4>{{ info.name }}</h4>
    <div class="font-weight-bold">{{ info.archetype }}</div>

</div>

</template>


<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;




</style>