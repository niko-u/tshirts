<template>

        <li>
             <div class="container bcontent">
                <div class="card" style="width: 60%;">
                    <div class="row no-gutters">
                        <div class="col-sm-5">


                            <div :id="setId(shirt.id)" class="carousel slide" data-bs-interval="false">
                            <div class="carousel-inner">
                                <div class="carousel-item active">
                                    <img :src="getImgUrl(shirt.images[0])" class="d-block w-100" alt="...">
                                </div>
                                <div class="carousel-item">
                                    <img :src="getImgUrl(shirt.images[1])" class="d-block w-100" alt="...">
                                </div>

                            </div>
                            <button class="carousel-control-prev" type="button" :data-bs-target="getId(shirt.id)" data-bs-slide="prev">
                                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                                <span class="visually-hidden">Previous</span>
                            </button>
                            <button class="carousel-control-next" type="button" :data-bs-target="getId(shirt.id)" data-bs-slide="next">
                                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                                <span class="visually-hidden">Next</span>
                            </button>
                            </div>




                        </div>
                        <div class="col-sm-7">
                            <div class="card-body">
                                <h5 class="card-title"> {{ shirt.title }} | <a class="artist" href="">@{{ shirt.artist }}</a></h5>
                                    <p class="card-text"> {{ shirt.description }} </p>
                                <hr>
                                <div id="upvotes">
                                    Upvotes: <button type="button" class="btn btn-outline-success" @click="upvote(shirt)"> {{ upvoteCount }} </button>
                                </div>
                                <div id="design">
                                    Design ID: {{ shirt.id }}
                                </div>
                                <div id="bottom">
                                    <p id="tags">tags: </p>
                                    <div id="tags" v-for="tag in shirt.tags" :key="tag">
                                        <button type="button" class="btn btn-success btn-sm"> {{ tag }} </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </li>
    
</template>

<script>

//data-bs-target="#carouselExampleControls"

export default {
    data() {
        return {
            upvoteCount: this.shirt.upvotes
        }
    },
    props: {
        shirt: Object
    },
     methods: {
        getImgUrl(image) {
            return new URL(`${image}`, import.meta.url).href
        }, 
        getId(ID) {
            return "#" + "a" + ID
        },
        setId(ID) {
            return "a" + ID
        },
        upvote(shirt) {
            shirt.upvotes += 1
            this.upvoteCount = shirt.upvotes
            console.log(shirt.upvotes)
        }
    },
}

</script>

<style scoped>
.artist {
    text-decoration: none;
    color: #89cc95;
}


#bottom {
    position: absolute;
    bottom: 0px;
}

.card-title {
    text-align: left;
}

.card-text {
    text-align: left;
}

#upvotes {
    float: left;
}

#tags {
    display: inline;
    margin-right: 5px;
}

#design {
    padding-top: 6px;
}
</style>
