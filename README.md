using:
```
<template>
  <div id="app">
    <MultiTrackPlayer :playersOptions="playersOptions"/>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import MultiTrackPlayer from "@psy21d/multiplayer";

export default defineComponent({
  name: 'ServeDev',
  components: {
    MultiTrackPlayer
  },
  data() {
    return {
      playersOptions: {
        playerA: {
          file: "https://github.com/psy21d/wavesurfer-example/blob/main/public/audio/Bass.mp3?raw=true",
          caption: "Bass.mp3",
        },
        playerB: {
          file: "https://github.com/psy21d/wavesurfer-example/blob/main/public/audio/Drums.mp3?raw=true",
          caption: "Drums.mp3",
        },
        playerC: {
          file: "https://github.com/psy21d/wavesurfer-example/blob/main/public/audio/Piano.mp3?raw=true",
          caption: "Piano.mp3",
          plugins: {
            timeline: true,
          }
        }
      },
      speed: 100,
    }
  },
});
</script>
```