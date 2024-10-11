<template>
  <div id="app">
    <div class="nav" id="nav">
      <router-link to="/"><img src="./assets/logo.svg" alt=""></router-link>
      <div class="contacts-login">
        <router-link to="/about" style="size: 15px;">Контакты</router-link>
        <router-link v-if="authenticated" to="/login" v-on:click.native="logout()"
          replace><button>Выйти</button></router-link>
        <router-link v-else to="/login"><button>Войти</button></router-link>
      </div>
    </div>
    <router-view @authenticated="setAuthenticated" />
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      authenticated: false,
      mockAccount: {
        username: "12345678",
        password: "12345678"
      }
    }
  },
  methods: {
    setAuthenticated(status) {
      this.authenticated = status;
    },
    logout() {
      this.authenticated = false;
    }
  }
}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1305px;
  padding: 18px 70px;
  border-bottom: 1px solid #000000;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding-right: 10px;
  text-decoration: none;
}

#nav button {
  border: 2px solid #FF685B;
  padding: 8px 60px;
  background: none;
  color: #FF685B;
  font-family: Montserrat;
  font-size: 20px;
  font-weight: 500;
  line-height: 24.38px;
  text-align: center;

}

#nav a.router-link-exact-active {
  color: #42b983;
}

.contacts-login {
  display: flex;
  gap: 50px;
  align-items: center;
}

@media (max-width: 375px) {
  .container {
    padding: 0;
    max-width: 320px;
  }

  #nav {
    padding: 22px 10px;
    margin-bottom: 40px;
  }

  .contacts-login {
    gap: 10px;
  }

  #nav button {
    padding: 6px 20px;
    border-radius: 7px;
  }
}
</style>
