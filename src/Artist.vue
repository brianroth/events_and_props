<template>
  <div class="container artist">
    <div class="artist-name">
      <a :href="artist.url">{{artist.name }}</a>
    </div>
    <div class="artist-likes">{{artist.likes }} Likes</div>
    <p>{{artist.blurb }}</p>
  </div>
</template>

<style>
.artist-likes {
  font-size: 85%;
}
.artist {
  margin-bottom: 1em;
}
.artist-name {
  font-size: 2em;
  font-weight: 500;
}
</style>

<script>
import EventHub from './EventHub.js'

export default {
  props: ['artist'],
  created () {
    EventHub.$on('liked', this.onLiked);
    EventHub.$on('disliked', this.onDisLiked);
  },
  methods: {
    onLiked: function() {
      this.artist.likes++;
    },
    onDisLiked: function() {
      this.artist.likes--;
    }
  }
}
</script>

