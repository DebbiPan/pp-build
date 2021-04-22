<template>
  <div>Tabs组件</div>
</template>

<script lang="ts">
import Tab from "./Tab.vue"
export default {
  setup(props,context){
    const defaults = context.slots.default()
    defaults.forEach((tag)=>{
      if(tag.type !== Tab){
        throw new Error('Tabs子标签必须是Tab')
      }
    })
    return {
      defaults
    }
  }
}
</script>