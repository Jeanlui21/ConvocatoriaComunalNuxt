<template lang="html">
  <div>
    <h5>{{ album.title }}</h5>
    <a :href="'/albums/' + album.id">Ver álbum</a>
  </div>
</template>

<script>
export default {
  name: 'AlbumCard',
  props: {
    album: Object
  }
}
</script>

<style lang="css">

</style>
