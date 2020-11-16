<template>
  <div id="app">
    <div class="container">
      <div class="nav">
        <img src="@/assets/logo.png" alt="" class="nav nav__avatar">
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
        <div class="nav nav__item">
          <label>1</label>
        </div>
      </div>
      <div class="content">
        <header class="header">
          <div class="header header__item">
            <label>1</label>
          </div>
          <div class="header header__item">
            <label>1</label>
          </div>
        </header>
        <div class="main"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {},
};
</script>

<style lang="scss">
body {
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  display: flex;
  height: 100%;
  flex-direction: row;
}
.container {
  display: flex;
  flex-grow: 1;
}
.nav {
  border: 1px black solid;
  height: 100%;
  width: 50px;

  /** FLEX */
  flex: 0 0 50px;
  display: flex;
  flex-direction: column;

  &__avatar {
    flex: 0 0 49px;
    width: 49px;
    height: auto;
    border-radius: 50%;
  }

  &__item {
    border: 1px pink solid;
  }
}
.content {
  border: 1px red solid;
  height: 100vh;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.header {
  height: 40px;
  border: 1px blue solid;

  /** FLEX */
  display: flex;
  flex-direction: row;
  flex-grow: 0;
  flex-basis: 0;

  &__item {
    border: 1px orange solid;
    flex-grow: 1;
  }
}
.main {
  flex-grow: 1;
  border: 2px green solid;
  display: flex;
}
</style>
