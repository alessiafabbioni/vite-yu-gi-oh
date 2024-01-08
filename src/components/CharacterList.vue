<script>
import SingleCharacter from './SingleCharacter.vue';

//importo store
import { store } from '../store';

export default {
    name: 'CharacterList',
    components: {
        SingleCharacter
    },
    data() {
        return {
        store,
        }
    }

}


</script>

<template>
    <section>
        <div class="container">
            <div class="row">
                <!-- prototipo da ripetere -->
                <div v-for="card in store.cardList" :key="card.id" class="col-6 col-md-4 col-lg-3 mb-5">
                    <SingleCharacter :info="card"/>

                </div>

            </div>

        </div>
    </section>



</template>


<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;




</style>