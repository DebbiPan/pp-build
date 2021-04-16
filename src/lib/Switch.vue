<template>
  <button @click="toggle" :class="{checked}"><span></span></button>
</template>

<script lang="ts">
import {ref} from 'vue';

export default {
  setup(){
    const checked = ref(false)
    const toggle = () =>{
      checked.value = !checked.value
    }
    return {checked,toggle}
  }
}
</script>

<style lang="scss" scoped>
$h:22px;
$h2:$h - 4px;
button{
  height:$h;
  width:$h*2;
  border:none;
  background:#888;
  border-radius:$h/2;
  position: relative;
}
span{
  position: absolute;
  height:$h2;
  width:$h2;
  background: #fff;
  top:2px;
  left:2px;
  border-radius: $h2/2;
  transition: left 250ms;
}
button:focus{
  outline: none;
}
button.checked{
  background: #1890FF;
}
button.checked > span{
  left:calc(100% - #{$h2} - 2px)
}
</style>