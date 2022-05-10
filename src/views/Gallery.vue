<template>
    <h1 id="title">What's Hot</h1>
    <ul id="gallery" v-for="shirt in data" :key="shirt.id">
        <Submission :shirt="shirt"></Submission>
    </ul>



</template>

<script>
import data from "/db/db.json";
import Submission from '/Users/nikourban/Desktop/tshirts/src/components/Submission.vue'
export default {
    created() {
        this.data = data;
    },
    data() {
        return {

        }
    },
    methods: {
 
    },
    components: {
        Submission
    }
}

</script>

<style scoped>

#title {
    margin-top: 7%;
    margin-bottom: 2%;
}

#id {
    margin-top: 200px;
}


</style>
