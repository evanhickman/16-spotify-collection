<template lang="html">
  <div class="app">
      <div class="container">
        <div class="box">
          <div class="panel">
            <p class="panel-heading">
              All the Paul Things
            </p>
            <song-item v-for="current in tracks" v-bind:track="current"></song-item>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import SongItem from './song-item.vue';

export default {
  components: {
    SongItem,
  },

  created() {
    fetch('https://api.spotify.com/v1/search?query=paul&type=track&offset=0&limit=20')
    .then(res => res.json())
    .then((data) => {
      this.tracks = data.tracks.items;
    });
  },

  data() {
    return {
      tracks: [
        { artist: 'Paul Simon', name: 'Graceland' },
        { artist: 'Paul Simon', name: 'Mother Child Reunion' },
        { artist: 'Paul Simon', name: 'Gumboot Whatever' },
      ],
    };
  },

  methods: {

  },
};
</script>
