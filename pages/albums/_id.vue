<template lang="html">
  <div class="row mx-0">
    <div class="col-4 mb-4" v-for="photo in photos" :key="photo.id">
      <div class="card">
        <div class="card-header">
          {{ photo.title }}
        </div>
        <div class="card-body d-flex justify-content-center">
          <img :src="photo.url" alt="img-photo" height="50">
        </div>
        <div class="card-footer">
          <a class="btn btn-outline-warning" href="/">
            Regresar
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios';
import env from "@/config/env";
import router from 'vue-router';

export default {
  name: 'AlbumIndvPage',
  data() {
    return {
      album: {},
      photos: []
    }
  },

  created() {
    let albumId = this.$route.params.id;
    axios.get(`${env.endpoint}/albums/${albumId}`).then(
        response => {
          this.album = response.data;
        }
    );

    axios.get(`${env.endpoint}/albums/${albumId}/photos`).then(
        response => {
          this.photos = response.data;
        }
    );
  }
}
</script>

<style lang="css" scoped>
.col-4 .card {
  min-height: 250px;
}
</style>
