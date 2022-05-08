<template>

 <div class="container bcontent">
        <div class="card" style="width: 800px;">
            <div class="row no-gutters">
                <div class="col-sm-5">
                    <img class="card-img" src="../assets/shirt.jpeg" alt="tshirt">
                </div>
                <div class="col-sm-7">
                    <div class="card-body">
                        <h5 class="card-title"> {{ title }} Design Title | <a class="artist" href="">@artist {{ artist }}</a></h5>
                            <p class="card-text"> {{ description }} This tshirt was designed to be the best quality design possible</p>
                        <hr>
                            <button type="button" class="btn btn-outline-success"> 9999 {{ votes }} </button>

                        <div id="bottom">
                            <p id="tags">tags: </p>
                            <div v-for="tag in tags">
                                <a href="tag.link"> {{ tag.title }} </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>





</template>

<script>

export default {
    data() {
        
    }
}

</script>

<style scoped>

.artist {
    text-decoration: none;
    color: #89cc95;
}

#tags {
    float: left;
}

#bottom {
    position: absolute;
    bottom: 0px;
}

#left {
    float: right;
}

#right {
    float: right;
}



</style>
