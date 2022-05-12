<template>
    <div class="player">
        <video controls autoPlay crossOrigin="anonymous">
            <source :src="`https://streaming-2dc2c.el.r.appspot.com/videos/video/${vidName}`" type="video/mp4">
            <track style="display:flex;align-items:center;justify-content:center" label="English" kind="captions" srcLang="en" :src="`https://streaming-2dc2c.el.r.appspot.com/videos/video/${vidName}/caption`" default>
        </video>
    </div>
</template>

<script>
export default {
 data() {
      return {
        vidName: ''
      }
    },
mounted(){
    this.vidName = this.$route.params.name
}
}
</script>

<style scoped>
.player{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 2em;
}
</style>