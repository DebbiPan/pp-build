<template>
  <div class="topnav">
    <div class="toggleAside" @click="toggleMenu">
      <img src="../assets/img/list.png" alt="列表">
    </div>
    <div class="logo">
      <router-link to="/">
        <img src="../assets/img/logopic.png" alt="logo">
      </router-link>
    </div>
    <ul class="menu">
      <li>菜单1</li>
      <li>菜单2</li>
    </ul>
  </div>
</template>

<script lang="ts">
import {inject, Ref} from 'vue';

export default {
  setup() {
    const asideVisible = inject<Ref<boolean>>('asideVisible');
    const toggleMenu = () => {
      asideVisible.value = !asideVisible.value;
    };
    return {toggleMenu};
  }
};
</script>

<style lang="scss" scoped>
img {
  width: 32px;
  height: 32px;
}

.topnav {
  background: #ffffff;
  display: flex;
  padding: 16px;
  border-bottom: 1px solid #DCDFE6;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10;
  justify-content: center;
  align-content: center;

  > .toggleAside {
    display: none;
    position: absolute;
    left: 16px;


  }

  > .logo {
    max-width: 6em;
    margin-right: auto;

    > img {
      max-width: 32px;
      max-height: 32px;

      &:hover {
        cursor: pointer;
      }
    }
  }

  > .menu {
    display: flex;
    white-space: nowrap;
    flex-wrap: nowrap;
    color: #8CC4FD;
    position: absolute;
    right: 16px;

    > li {
      margin: 0 1em;
      line-height: 32px;
    }
  }

  @media (max-width: 500px) {
    .menu {
      display: none;
    }
    .logo {
      margin: 0 auto;
    }
    .toggleAside {
      display: inline-block
    }
  }
}
</style>