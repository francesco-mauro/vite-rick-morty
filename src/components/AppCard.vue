<script>
export default {
    props: {
        cardObj: Object,
    }
}
</script>

<template>
    <div class="card">
        <img :src="cardObj.image" class="card-img-top" alt="Character Image">
        <div class="card-body">
            <h5 class="card-title">{{ cardObj.name }}</h5>
            <p class="card-text">{{ cardObj.species }} - {{ cardObj.status }}</p>
            <a href="#" class="btn btn-primary">Learn more</a>
        </div>    
    </div>
</template>

<style lang="scss" scoped>
</style>
