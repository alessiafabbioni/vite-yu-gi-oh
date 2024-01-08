<script >
import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import CharacterList from './components/CharacterList.vue'

export default {
  components: {
      AppHeader,
      AppSearch,
      CharacterList
  }
}

</script>

<template>
  <AppHeader message="Yu-Gi-Oh"/>
  <main>
    <AppSearch/>
    <CharacterList/>
  </main>
</template>

<style lang="scss">
@use './styles/general.scss';

main {
  padding-top: 20px;
}

</style>
