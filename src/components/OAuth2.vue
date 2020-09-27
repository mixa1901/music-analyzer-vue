<template>
  <div>
    <a v-bind:href="musicService.url">{{ musicService.name }}</a>
    <br>
  </div>
</template>

<script>
export default {
  props: {
    musicService: {
      type: Object,
      required: true
    }
  }
}
</script>