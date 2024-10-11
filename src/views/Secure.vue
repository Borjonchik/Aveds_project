<template>
  <div class="container secure">
    <h1 class="account_title">
      Привет, Сергей
    </h1>
    <div class="buttons">

      <router-link to="/login" v-on:click.native="logout()" replace><button>Выйти из аккаунта</button></router-link>
      <router-link to="/about"><button>перейти в контакты</button></router-link>
    </div>
  </div>

</template>


<script>
export default {
  name: 'Secure',
  data() {
    return {}
  },
  mounted() {
    if (!this.$parent.authenticated) {
      this.$router.replace({ name: "Login" });
    }
  },
  methods: {
  }
}
</script>

<style>
.secure {
  padding: 141px 197px;
}

.account_title {
  width: 100%;
}
</style>