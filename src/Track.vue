<template>
   <div class="track">
    {{track.number}}. {{track.title}}
    <small>{{ track.length | lengthFormat }}</small><span v-on:click.prevent="like" v-bind:class="{ liked: track.liked }" class="glyphicon glyphicon-heart"/>
   </div>
</template>

<style>
.glyphicon-heart {
    padding-left: 5px;
    color:white;
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}

.glyphicon.liked {
  text-shadow: none;
  color: red;
}
</style>

<script>
import EventHub from './EventHub.js'

export default {
  methods: {
    like: function(event) {
      if (this.track.liked) {
        this.track.liked = false;
        EventHub.$emit('disliked', this.track)
      } else {
        this.track.liked = true;
        EventHub.$emit('liked', this.track)
      }
    }
  },
  props: ['track'],
  filters: {
    lengthFormat: function (value) {
      if (!value) return ''
      return  Math.floor(value / 60) + ':' + value % 60
    }
  }
}
</script>

