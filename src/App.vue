<template>
  <div>
    <SideBarSec />
  </div>
</template>

<script>
import SideBarSec from './components/SideBarSec.vue'

export default {
  components: {
    SideBarSec,
  },
};
</script>
<style lang="scss" scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
