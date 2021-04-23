<template>
  <button @click="toggle" :class="{checked:value}" :disabled="disabled"><span></span></button>
</template>

<script lang="ts">

export default {
  props:{
    value:{
      type:Boolean
    },
    disabled:{
      type:Boolean,
      default:false
    }
  },
  setup(props,context){
    const toggle = () =>{
      context.emit('update:value',!props.value)
    }
    return {toggle}
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
  background:#aaa;
  border-radius:$h/2;
  position: relative;
  &[disabled]{
    cursor: not-allowed;
    background:darkred;
  }
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
  background: #FFAFC9;
}
button.checked > span{
  left:calc(100% - #{$h2} - 2px)
}
</style>