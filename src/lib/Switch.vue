<template>
  <button><span></span></button>
</template>

<script lang="ts">

</script>

<style lang="scss" scoped>
$h:22px;
$h2:$h - 4px;
button{
  height:$h;
  width:$h*2;
  border:none;
  background:#1890FF;
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
}
button:hover > span{
  left:calc(100% - #{$h2} - 2px)
}
</style>