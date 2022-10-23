<template>
    <a v-bind:href="url">
        <div class="button">
            <p>{{title}}</p>
        </div>
    </a>
</template>

<script>
export default {
  props: ['title','url']
}
</script>