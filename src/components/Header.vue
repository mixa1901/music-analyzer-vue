<template>
  <div>
    <p>Login via: </p>
    <OAuth2
        v-for="musicService in musicServices" :key="musicService.id"
        v-bind:musicService="musicService"
    />
  </div>
</template>

<script>
import OAuth2 from '@/components/OAuth2'
export default {
  props: ["musicServices"],
  components: {
    OAuth2
  }
}
</script>