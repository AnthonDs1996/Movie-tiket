<template>
    <div class="movie-detail">
        <img :src="movieImage" alt="Movie">
        <p>{{ movieTitle }}</p>
    </div>
</template>

<script>
export default {
    props: ["movie"],
    data () {
        return {
            movieTitle: this.movie.title,
            movieImage: require(`../assets/${this.movie.imageName}`)
        }
    }
}
</script>


<style scoped>
    .movie-detail img {
  border-radius: 20px;
  width: 230px;
  height: 350px;
}

.movie-detail {
  margin: 7px;
}

.movie-detail p {
  margin-top: 15px;
  font-weight: 1000;
}
</style>