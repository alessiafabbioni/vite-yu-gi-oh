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
        <div class="ms-dropdown input-group">
                <input type="text" class="form-control" placeholder="Search your card" aria-label="card search" v-model.trim="store.searchText">
                <button class="btn btn-primary" type="button" @click.prevent="$emit('performSearch')">Search</button>
                <button class="btn btn-warning" type="button"@click='resetSearch'>Reset</button>
        </div>
        
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