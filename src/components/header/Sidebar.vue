<template>
  <div class="sidebar">
    <div
      class="sidebar-backdrop"
      @click="closeSidebarPanel"
      v-if="isPanelOpen"
    ></div>
    <transition name="slide">
      <div v-if="isPanelOpen" class="sidebar-panel">
        <slot></slot>
      </div>
    </transition>
  </div>
</template>

<script>
import {store, mutations} from '@/store.js'

export default {
//   data: () => ({
//     isPanelOpen: true,
//   }),
computed:{
    isPanelOpen(){
        return store.isNavOpen
    }
},
  methods: {
    closeSidebarPanel() {
    //   this.isPanelOpen = false;
        mutations.toggleNav()
    },
    //  closeSidebarPanel: mutations.toggleNav
  },
};
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.slide-enter-active,
.slide-leave-active {
  transition: all 0.2s;
}

.slide-enter-from,
.slide-leave-to {
  /* transform: translateX(-100%); */
  opacity: 0;
  transition: all 0.5s;
}

.sidebar-backdrop {
  /* background-color: rgba(0, 0, 0, 0.5); */
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  cursor: pointer;
}

.sidebar-panel {
  overflow-y: auto;
  background-color: $background-color;
  position: fixed;
  left: 0;
  top: 100px;
  height: 100vh;
  z-index: 999;
  padding-top: 20px;
  width: 100vw;
}
</style>