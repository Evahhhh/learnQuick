<template>
    <div class="content-card">
        <p>Audio</p>
        <div class='audio-player'>
            <AudioPlayer 
            :option="{
                src: '/f1-piano.mp3',
                title: 'Piano F1',
                coverImage: '/f1-piano-cover.png',
            }" />
        </div>
    </div>
</template>

<script>
import AudioPlayer from 'vue3-audio-player'
import 'vue3-audio-player/dist/style.css'

export default {
    name: 'FilesAudio',
    components: {
        name : 'AudioPlayer',
        AudioPlayer,
    },
}
</script>

<style>
.content-card{
    background : white;
    text-align : center;
    margin-top : 30px;
}

</style>