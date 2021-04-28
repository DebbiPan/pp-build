# 开始使用

请先&nbsp;[安装](#/doc/install-build)&nbsp;本组件库。
然后在你的代码中写入下面的代码：

```
import {Button, Tabs, Switch, Dialog,openDialog} from "ppbuild-ui"
```

## Vue 单文件组件
代码示例：
```js
<template>
  <div>
    <Button>按钮</Button>
  </div>
</template>
<script>
  import {Button, Tabs, Switch, Dialog,openDialog} from "ppbuild-ui"
  export default {
  components:{Button}
}
</script>
```

**请注意**

在组件示例中所提供的代码在你的项目中需要调整。如引入组件时所使用的路径并不能在你的项目中正确引入，应该参照本页的引入组件代码。
