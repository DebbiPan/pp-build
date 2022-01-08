<template>
  <div>
    <div class="topnavAndBanner">
      <TopNav/>
      <div class="banner">
        <h1>PPBuild-UI</h1>
        <h2>一个实用的UI框架</h2>
        <p class="actions">
          <a href="https://github.com/DebbiPan/pp-build">Github</a>
          <router-link to="/doc">开始</router-link>
        </p>
      </div>
    </div>
    <div class="features">
      <ul>
        <li>
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-vue"></use>
          </svg>
          <h3>基于 Vue 3</h3>
          <p>使用了Vue 3 Composition API</p>
        </li>
        <li>
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-typescript"></use>
          </svg>
          <h3>基于 TypeScript</h3>
          <p>源代码采用 TypeScript书写</p>
        </li>
        <li>
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-light"></use>
          </svg>
          <h3>代码易读</h3>
          <p>每个组件的源代码都极其简洁</p>
        </li>
      </ul>
    </div>
  </div>
</template>


<script lang="ts">
import TopNav from '../components/Topnav.vue';

export default {
  components: {TopNav},

};
</script>

<style lang="scss" scoped>
$blue: #269FDF;
.topnavAndBanner {
  background: rgb(201, 237, 253);
  background: linear-gradient(163deg, rgba(201, 237, 253, 1) 0%, rgba(207, 240, 255, 1) 58%, rgba(236, 249, 255, 1) 100%);
  clip-path: ellipse(80% 60% at 50% 40%);

  > .banner {
    padding: 100px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

    > .actions {
      padding: 8px 0;

      a {
        margin: 3px 8px;
        display: inline-block;
        border-radius: 10px;
        padding: 3px 14px;
        border: 1px solid #8CC4FD;
        background: $blue;
        color: #fff;
      }
    }
  }
}

.features {
  margin: 64px auto;
  padding: 0 16px;

  @media (min-width: 800px) {
    width: 800px;
    >ul {
      >li {
        width: 50%;
      }
    }
  }
  @media (min-width: 1200px) {
    width: 1200px;
    >ul {
      >li {
        width: 33.3333%;
      }
    }
  }
  >ul{
    display: flex;
    flex-wrap: wrap;
    >li{
      margin:16px 0;
      display:grid;
      justify-content: start;
      align-content: space-between;
      grid-template-areas: "icon title" "icon text";
      grid-template-columns: 80px auto;
      grid-template-rows: 1fr auto;
      >svg{
        grid-area:icon;
        width:64px;
        height:64px;
      }
      >h3{
        grid-area: title;
        font-size:28px;
      }
      >p{
        grid-area:text;
      }
    }
  }
}


.icon {
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>