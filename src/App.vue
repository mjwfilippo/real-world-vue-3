<template>
  <div id="flashMessage" v-if="GStore.flashMessage">
    {{ GStore.flashMessage }}
  </div>
  <nav>
    <router-link :to="{ name: 'EventList' }">Events</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link>
  </nav>
  <router-view />
</template>

<script>
export default {
  inject: ["GStore"]
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.no-text-dec {
  text-decoration: none;
  color: #42b983;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

h4 {
  font-size: 20px;
}

.btn {
  display: inline-flex;
  padding: 15px 50px;
  background-color: #42b983;
  color: white;
  border: 1px solid #42b983;
  border-radius: 10px;
  font: bold 1.17em/1.5em Avenir, sans-serif;
  text-decoration: none;
}

.animation {
  rotate: x 0deg;
  scale: 1;
  transition: 0.1s ease-in-out;
}

.animation:hover {
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
  rotate: x 10deg;
  scale: 1.04;
  transition: 0.1s ease-in-out;
}

#flashMessage {
  animation: yellowfade 3s;
}

@keyframes yellowfade {
  from {
    background: rgb(164, 235, 171);
  }
  to {
    background: transparent;
  }
}
</style>
