<template>
  <video />
</template>

<script>
export default {
  data() {},
  methods: {
    startCamera() {
      // Prefer camera resolution nearest to 1280x720.
      var constraints = { audio: true, video: { width: 360, height: 360 } };

      navigator.mediaDevices
        .getUserMedia(constraints)
        .then(function(mediaStream) {
          var video = document.querySelector("video");
          video.srcObject = mediaStream;
          video.onloadedmetadata = function(e) {
            if (e) console.log(e);
            video.play();
          };
        })
        .catch(function(err) {
          console.log(err.name + ": " + err.message);
        }); // always check for errors at the end.
    }
  },
  mounted() {
    this.startCamera();
  }
};
</script>