<template>
  <div class = "page">
    <link
        href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
        rel="stylesheet"
      />
      <NavBar />
      <div class = "content">
        <IndexWelcome />
      </div>  
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({

})
</script>

<style>


.content{
  display : flex;
  background-image: url("~/static/assets/laptop-woman-books.jpg");
  background-position : center center;
  background-size : cover;
  height : 92vh;
  align-items : center;
}
</style>