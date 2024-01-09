<script>
import {store} from '../store';

export default {
    name: 'AppSearch',
    data () {
        return {
            store,
        }
    },

    methods: {
        resetSearch() {
            store.searchText = "";
            this.$emit('performSearch');
        } 
    }

}


</script>

<template>
    <section>
        
        <select class="form-select" aria-label="Default select example" v-model="store.selectedArchetype" @change="$emit('archSelected')">
            <option selected disabled value="">Open this select menu</option>
            <option v-for="archetype in store.archetypes" :key="archetype.id" :value="archetype.id">{{ store.archetypes[0].archetype_name }} </option>

        </select>
        
    </section>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

section {
    background-color: $bg-color;
    width: 100%;


}

.ms-dropdown {
    padding: 2rem 30rem;
        
    }



</style>