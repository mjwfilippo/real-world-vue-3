<template>
  <nav>
    <router-link :to="{ name: 'EventList' }">Events</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link> |
    <router-link :to="{ name: 'EventCreate' }">Create Event</router-link>
  </nav>
  <router-view />
</template>

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

h2 {
  font-size: 40px;
  font-weight: 700;
}

h3 {
  font-size: 25px;
  font-weight: 700;
}

h4 {
  font-size: 20px;
  font-weight: 700;
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
  animation: greenfade 3s;
}

input {
  display: block;
  width: 100%;
  height: 30px;
  margin-bottom: 24px;
}

input[type="text"] {
  padding: 0 10px;
}

input:focus {
  border-color: #16c0b0;
  outline: 0;
}

button {
  align-items: center;
  height: 50px;
  padding: 0 40px;
  background: linear-gradient(to right, #16c0b0, #84cf6a);
  color: #fff;
  border: none;
  border-radius: 6px;
  font-size: 18px;
  font-weight: 800;
  cursor: pointer;
  transition: all 0.2s linear;
}

button:hover {
  -webkit-transform: scale(1.02);
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}

.form-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  margin-bottom: 10%;
}

select:focus {
  border-color: #16c0b0;
  outline: 0;
}

@keyframes greenfade {
  from {
    background: #63e8ac;
  }
  to {
    background: transparent;
  }
}
</style>
