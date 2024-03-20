<template>
  <router-link :to="{ name: 'home' }">
    <img
      src="@/assets/images/logo/logo-c.png"
      alt=""
      v-if="!this.$store.themeSettingsStore.isDark"
    />

    <img
      src="@/assets/images/logo/logo-c-white.png"
      alt=""
      v-if="this.$store.themeSettingsStore.isDark"
    />
  </router-link>
</template>
<script></script>
