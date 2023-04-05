<template>
  <header class="header">
    <nav>
      <img src="@/assets/images/menu.svg" v-on:click="showMenu()" />
      <h1>Thrifted Swag</h1>
      <img src="@/assets/images/account-circle-filled.svg" />
      <div class="menu" v-show="active">
        <ul>
          <li><a href="">Home</a></li>
          <li><a href="">Shop</a></li>
          <li><a href="">Trading</a></li>
          <li><a href="">Account</a></li>
          <li><a href="">Sign Up</a></li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script setup>
let active = false;

const showMenu = () => {
  console.log("clicked");
  active = !active;
  console.log(active);
  const menuDiv = document.querySelector(".menu");
  if (active) {
    menuDiv.classList.add("show");
  } else {
    menuDiv.classList.remove("show");
  }
};
</script>

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

  nav {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 8px 4px;
    gap: 6px;
    width: 100%;
    height: 64px;

    .menu {
      left: 0;
      width: 100%;
      color: black;
      position: absolute;
      top: 84px;
      background-color: white;
      z-index: 1000;
      padding: 1rem 0 0 1rem;
      height: 100%;
      display: none;

      ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: column;
        gap: 1rem;

        li {
          font-size: 1.5rem;
          font-weight: 500;
          color: black;

          a:hover {
            color: $dark-on-primary;
            text-decoration: underline;
          }
        }
      }
    }
    .menu.show {
      display: block;
    }
  }
}
</style>
