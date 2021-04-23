# 开始使用

请先&nbsp;[安装](#/doc/install-build)&nbsp;本组件库。
然后在你的代码中写入下面的代码

```
import {Button, Tabs, Switch, Dialog} from "ppbuild-ui"
```

## Vue 单文件组件
代码示例：
```js
<template>
  <div><Button>按钮</Button></div>
</template>
<script>
  import {Button, Tabs, Switch, Dialog} from "king-ui"
  export default {
  components:{Button}
}
</script>
```
