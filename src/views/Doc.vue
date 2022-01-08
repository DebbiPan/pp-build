<template>
  <div class="layout">
    <TopNav class="nav"/>
    <div class="content" >
      <aside v-if="asideVisible">
        <h2>文档</h2>
        <ol>
          <li>
            <router-link to="/doc/intro">介绍</router-link>
          </li>
          <li>
            <router-link to="/doc/install-build">安装</router-link>
          </li>
          <li>
            <router-link to="/doc/get-start">开始使用</router-link>
          </li>
        </ol>
        <h2>组件列表</h2>
        <ol>
          <li>
            <router-link to="/doc/switch">Switch组件</router-link>
          </li>
          <li>
            <router-link to="/doc/button">Button组件</router-link>
          </li>
          <li>
            <router-link to="/doc/dialog">Dialog组件</router-link>
          </li>
          <li>
            <router-link to="/doc/tabs">Tabs组件</router-link>
          </li>
        </ol>
      </aside>
      <main>
        <router-view/>
      </main>
    </div>
  </div>
</template>

<script lang="ts">
import TopNav from '../components/Topnav.vue';
import {inject, Ref} from 'vue';

export default {
  components: {TopNav},
  setup() {
    const asideVisible = inject<Ref<boolean>>('asideVisible');
    return {asideVisible};
  }
};
</script>

<style lang="scss" scoped>

.layout{
  display:flex;
  flex-direction: column;
  height:100vh;
  > .nav{
    flex-shrink: 0;
    background:#ECF9FF;
    z-index:11;
  }
  > .content{
    flex-grow: 1;
    padding-top:60px;
    padding-left: 156px;
    @media  (max-width:500px){
      padding-left: 0;
    }
  }
}
.content{
  display:flex;
  > aside{
    flex-shrink: 0;
    z-index: 10;
  }
  > main{
    flex-grow:1;
    padding:16px;
  }
}
aside {
  border-right:1px solid #eee;
  background: #fff;
  width: 150px;
  padding: 16px 0;
  position: fixed;
  left:0;
  height: 100%;
  > h2 {
    margin-bottom: 4px;
  }

  > ol {
    > li {
      >a{
        display: block;
        padding: 4px 16px;
      }
      & :hover {
        color: #333;
      }
      > .router-link-active{
        background:#ECF9FF;
        border-left: 3px solid #1F9CDD;
        padding-left: 13px;
      }
    }
  }
  main{
    overflow: auto;
  }
}

</style>



