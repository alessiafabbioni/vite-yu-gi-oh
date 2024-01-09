<script >
//importo axios
import axios from 'axios'

//importo componenti figli
import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import CharacterList from './components/CharacterList.vue'

//importo store
import { store } from './store';

export default {
  components: {
      AppHeader,
      AppSearch,
      CharacterList
  },
  data() {
    return {
      store,
      archetypes: [],
    }
  },
  methods: {
    getCards() {
      let myUrl = store.apiURL;
      let archUrl = store.archUrl;

      if(store.searchText !== "") {
        myUrl += `?${store.nameArch}=${store.searchText}`;      }


      axios
        .get(myUrl)
        .then((res => {
          //console.log(res.data.data);
          store.cardList = res.data.data;
        }))
        .catch((err)=>{
          console.log("Errori", err);
        })

      axios
        .get(archUrl)
        .then((res => {
          this.archetypes = res.data;
        }))

        .catch((err)=>{
          console.log("Errori", err);
        })
    }
  },
  created() {
    this.getCards();

  }
}

</script>

<template>
  <AppHeader message="Yu-Gi-Oh"/>
  <main>
    <AppSearch @performSearch="getCards"/>
    <CharacterList/>
  </main>
</template>

<style lang="scss">
@use './styles/general.scss';

main {
  padding-top: 20px;
}

</style>
