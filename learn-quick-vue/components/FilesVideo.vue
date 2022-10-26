<template>
    <div class="content-card-video">
        <h1>Vidéo</h1>
        <div class="video-player">
            <LazyYoutube src="https://youtu.be/dQw4w9WgXcQ" aspect-ratio="16:9" thumbnail-quality="standard" />
        </div>
    </div>
</template>

<script>
import {LazyYoutube} from 'vue-lazytube'

export default {
    name: 'FilesVideo',
    components: {
        LazyYoutube,
    },
}
</script>

<style>
.content-card-video{
    background : white;
    text-align  : center;
    margin-top : 30px;
}

.video-player{
    margin-top : 30px;
    margin-left : 10px;
    margin-right : 10px;
}
</style>