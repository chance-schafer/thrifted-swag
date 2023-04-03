<template>
  <header class="header">
    <img src="@/assets/images/menu.svg" />
    <h1>Thrifted Swag</h1>
    <img src="@/assets/images/account-circle-filled.svg" />
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
.header {
  /* Auto layout */

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 8px 4px;
  gap: 6px;
  width: 100%;
  height: 64px;
}
</style>
