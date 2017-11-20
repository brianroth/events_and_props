<template>
  <div class="row album">
    <div class="col-md-4">
      <img :src="album.image" class="album-art">
    </div>
    <div class="col-md-8">
      <div class="album-title">
        <a :href="album.url">{{ album.title }} ({{ album.year }})</a>
      </div>
      <div class="album-blurb">
        {{ album.blurb }}
      </div>
      <ul class="album-tracklist">
        <li v-for="track in album.tracks">
          <app-track :track="track"></app-track>
        </li>
      </ul>
    </div>
  </div>
</template>

<style>
.album-art {
  width: 300px;
  height: 300px;
}
.album {
  margin-bottom: 1em;
}
.album-blurb {
  margin-bottom: 1em;
}
.album-title {
  font-size: 2em;
  font-weight: 500;
}
.track {
  font-size: 1.1em;
}
small {
  font-size: 65%;
}
ul.album-tracklist {
    -moz-column-count: 2;
    -moz-column-gap: 20px;
    -webkit-column-count: 2;
    -webkit-column-gap: 20px;
    column-count: 2;
    column-gap: 20px;
    padding-left: 10px;
}
ul.album-tracklist li {
  list-style-type: none;
}
</style>

<script>
import Track from './Track.vue'

export default {
  props: ['album'],
  components: {
    'appTrack': Track
  }
}
</script>

