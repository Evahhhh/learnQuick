<template>
    <div class = navbar>
        <div class="navbar-content">
            <NavBarIndex title="Accueil" url = "/"> </NavBarIndex>
            <NavBarIndex title="Ma carte" url = "/map"> </NavBarIndex>
            <NavBarIndex title="Mes fichiers" url = "/files"> </NavBarIndex>
            <NavBarIndex title="Mes tâches" url = "/tasks"> </NavBarIndex>
            <NavBarIndex title="Mon quiz" url = "/quizz"> </NavBarIndex>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
@import 'https://fonts.googleapis.com/css2?family=Hubballi&display=swap';

.navbar{
    background-color: white;
    box-shadow: #D1D1D1 0 48px 100px 0;
    position : relative;
    z-index : 10;
}

.navbar-content{
    font-family: Hubballi, cursive;
    font-size : 28px;
    display: flex;
    justify-content : space-around;
    margin-left : 30px;
    margin-right : 30px;
    height : 8vh;
}
</style>