<template lang="html">
  <div class="">
    <div class="track panel-block track">
      <div class="media is-fullwidth">
        <div class="media-left">
          <p class="track__frame image">
            <img src="http://bulma.io/images/placeholders/64x64.png" alt="">
          </p>
        </div>
        <div class="media-content">
          <h2 class="title track__artist">{{ track.artist }}</h2>
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
