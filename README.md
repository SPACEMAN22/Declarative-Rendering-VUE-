# Declarative-Rendering-VUE-

Code 

HTML

<div id="vue-instance">
  <div v-if="isLoggedIn">
    HELLO WORLD!
    <button @click="login" type="submit">Logout</button>
  </div>
  <div v-else>
    <input type="text" placeholder="username">
    <input type="password" placeholder="password">
    <button @click="login" type="submit">Login</button>
  </div>
</div>

JAVASCRIPT/VUE

var vm = new Vue({
  el: '#vue-instance',
  data: {
    isLoggedIn: false
  },
  methods: {
    login: function() {
      // 'this' refers to the vm instance
      this.isLoggedIn = !this.isLoggedIn;
    }
  }
});
