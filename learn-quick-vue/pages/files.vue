<template>
    <div>
        <link
        href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
        rel="stylesheet"
        />
        <NavBar />
        <div class = "content">
            <div class = "card">
                <div class ="audio">
                    <FilesAudio/>
                </div>
                <div class ="video">
                    <FilesVideo/>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script lang="ts">
import Vue from 'vue';

export default Vue.extend({

})
</script>

<style>
.card {
    width: 90%;
    display: grid;
    background :#F7F2FF;
    grid-template-columns: 1fr 1fr;
    column-gap: 30px;
    margin-left : 5%;
    margin-right : 5%;
    padding : 50px;
    justify-content : center;
    font-size : 22px;
}

.audio{
    background : white;
    grid-column: 1;
    grid-row: 1;
    border-radius : 10px;
    width : auto;
    height : 74vh;
    box-shadow: #DBCBCB 0 8px 24px;
}

.video{
    background : white;
    grid-column: 2;
    grid-row: 1;
    border-radius : 10px;
    width : auto;
    height : 74vh;
    box-shadow: #DBCBCB 0 8px 24px;
}

.content{
    height : 92vh;
    background-color : #F7F2FF;
}
</style>