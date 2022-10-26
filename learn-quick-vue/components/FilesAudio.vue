<template>
    <div class="content-card">
        <p>Audio</p>
        <div class='audio-player'>
            <!-- <AudioPlayer 
            :option="{
                src: './f1-piano.mp3',
                // src: 'https://freetestdata.com/wp-content/uploads/2021/09/Free_Test_Data_100KB_MP3.mp3',
                title: 'Piano F1',
                coverImage: '/f1-piano-cover.png',
            }" />  -->
             <AudioPlayer
                    ref="audioPlayer"
                    :audio-list="audioList.map(elm => elm.url)"
                    :before-play="handleBeforePlay"
                    theme-color="#ff2929"
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
          name: 'Piano F1',
          url: './f1-piano.mp3'
        }
      ]
    }
}
}
</script>

<style>
.content-card{
    background : white;
    text-align : center;
    margin-top : 30px;
}

</style>