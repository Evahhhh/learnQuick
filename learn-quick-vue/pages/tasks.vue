<template>
    <div>
        <link
        href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
        rel="stylesheet"
        />
        <NavBar />
        <div class = todo-section>
            <div class = tasks-card>
                <TasksToDo />
            </div>
        </div>
    </div>
</template>
  
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({

})
</script>

<style>
.todo-section {
    height: 92vh;
    background-color: #F7F2FF;
}

.tasks-card {
    height : 74vh;
    width: 90%;
    border-radius : 10px;
    background : white;
    box-shadow: #DBCBCB 0 8px 24px;
    margin-left : 5%;
    margin-right : 5%;
    padding:20px;
}
</style>
