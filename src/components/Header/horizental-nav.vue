<template>
  <div class="main-menu">
    <DesktopMenuMain v-if="this.$store.themeSettingsStore.mode === 'dev' " />
    <DesktopMenu v-else />
  </div>
</template>
<script>
import DesktopMenu from "./Navtools/DesktopMenu";
import DesktopMenuMain from "./Navtools/DesktopMenuMain";
export default {
  components: {
    DesktopMenu,
    DesktopMenuMain
  },
};
</script>
<style lang=""></style>
