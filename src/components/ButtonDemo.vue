<template>
  <div>
    <Button>hello word </Button>
    <Button theme="button">hello world</Button>
    <Button theme="link">hello world</Button>
    <Button theme="text">hello world</Button>
  </div>
</template>

<script lang="ts">
import Button from "../lib/Button.vue"

export default {
  components:{Button}
}
</script>

<style lang="scss" scoped>

</style>