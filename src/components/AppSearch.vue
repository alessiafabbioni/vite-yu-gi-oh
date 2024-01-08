<script>
export default {
    name: 'AppSearch',

}


</script>

<template>
    <section>
        <div class="ms-dropdown dropdown container">
            <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                Cerca
            </button>
            <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Action</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
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
    padding: 2rem 0;
        
    }



</style>