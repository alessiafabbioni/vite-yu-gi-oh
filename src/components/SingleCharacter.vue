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
    <div class="card-info">
        <h4 class="text-uppercase">{{ info.name }}</h4>
            <div class="font-weight-bold text-center">{{ info.archetype }}</div>
            <div class="fst-italic p-2 text-center">{{ info.race }}</div>
    </div>
    

</div>

</template>


<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.character {
    background-color: $bg-color;
    height: 100%;
    
    h4 {
        color: white;
    }

}

.card-info {
    padding: 3px;

}




</style>