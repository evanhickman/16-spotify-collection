<template lang="html">
  <div class="">
    <div class="track panel-block track">
      <div class="media is-fullwidth">
        <div class="media-left">
          <p class="track__frame image">
            <img :src="track.album.images[0].url" alt="">
          </p>
        </div>
        <div class="media-content">
          <h2 class="title track__artist">{{ track.artists[0].name }}</h2>
          <h3 class="subtitle track__name">{{ track.name }}</h3>
        </div>
        <div class="media-right">
          <span class="icon is-large"><i class="fa fa-spotify"></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['track'],

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
