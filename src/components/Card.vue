<template>
  <div class="card">
    <h1>Hello World</h1>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.card {
  /* Auto layout */

  background-color: $dark-surface-container-low;
  display: flex;
  flex-direction: columns;
  padding: 0px;
  isolation: isolate;
  width: 360px;
  height: 480px;
  margin: 20px auto;

  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
  border-radius: 12px;

  order: 0;
  flex-grow: 0;

  h1 {
    margin: 0 auto;
    padding: 5px;
  }
}
</style>
