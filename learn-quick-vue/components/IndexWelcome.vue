<template>
    <div class = rectangle>
        <div class="rectangle-content">
            <p>Bienvenue sur</p>
            <p>Learn Quick</p>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.rectangle{
    display : flex;
    align-items : center;
    background-color : rgba(0 0 0 / 50%);
    width : 20%;
    height : 20%;
    border-radius : 0 10px 10px 0;
}

.rectangle-content{
    font-family: Hubballi, cursive;
    font-size : 28px;
    justify-content : center;
    margin-left : 30px;
    margin-right : 30px;
    color : white;
    text-align : center;
}

</style>