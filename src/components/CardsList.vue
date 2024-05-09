<script>
import axios from 'axios';
import AppCard from './AppCard.vue'

export default {
    components: {
        AppCard,
    },
    data() {
        return {
            cardsArray: [],
        };
    },
    created() {
        axios
        .get("https://rickandmortyapi.com/api/character")
        .then((response) => {
            this.cardsArray = response.data.results;
        })
    },
};
</script>

<template>
    <div class="container">
        <div class="row row-cols-1 row-cols-md-3 row-cols-lg-4">
            <div class="col" v-for="character in cardsArray" :key="character.id">
                <AppCard :cardObj="character"/>
            </div>
        </div>
    </div>
</template>

