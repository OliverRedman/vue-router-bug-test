<template>
  <div id="app">
    <div id="nav">
      <router-link class="sticky de" to="/">Home</router-link>
      <router-link class="sticky do" to="/about">About</router-link>
    </div>
    <transition mode="out-in" name="fade">
      <router-view />
    </transition>
  </div>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.1s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.de {
  left: 30px;
}
.do {
  left: 100px;
}
.sticky {
  position: fixed;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
