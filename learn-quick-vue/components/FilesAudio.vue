<template>
    <div class="content-card-audio">
        <p>Audio</p>
        <div class='audio-player'>
            {{ currentAudioName || audioList[0].name }}
            <AudioPlayer
            ref="audioPlayer"
                    :audio-list="audioList.map(elm => elm.url)"
                    :before-play="handleBeforePlay"
                    theme-color="#3A0082"
                />
        </div>
    </div>
</template>

<script>
import AudioPlayer from '@liripeng/vue-audio-player';
import 'vue3-audio-player/dist/style.css';

export default {
    name: 'FilesAudio',
    components: {
        AudioPlayer,
    },
    data() {
        return {
            currentAudioName: '',
            audioList: [
                {
                    name: 'Formula 1 Theme Piano Arrangement',
                    url: './f1-piano.mp3'
                },
                {
                    name: 'Avicii - Addicted To You',
                    url: './Avicii - Addicted To You.mp3'
                },
                {
                    name : 'Muse - Hysteria',
                    url : './Muse - Hysteria.mp3'
                },
                {
                    name : 'Linkin Park - In The End',
                    url : './Linkin Park - In The End.mp3'
                }
            ]
        }
    },
    methods: {
        // Something to do before playing
        handleBeforePlay(next) {
        // There are a few things you can do here...
        this.currentAudioName = this.audioList[this.$refs.audioPlayer.currentPlayIndex].name
        
        next() // Start playing
        }
    }
}

</script>

<style>
.content-card-audio{
    background : white;
    text-align  : center;
    margin-top : 30px;
}

.audio-player{
    font-size : 18px;
    margin-top : 30px;
    margin-left : 10px;
    margin-right : 10px;
}

</style>