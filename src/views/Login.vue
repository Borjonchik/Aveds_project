<template>
    <div class="login" id="login container">
        <h1>Login</h1>
        <div class="form-inputs">
            <label for="username">
                <input type="text" id="username" name="username" v-model="input.username" placeholder="Логин" />
            </label>
        </div>
        <div class="form-inputs">
            <label for="password">
                <input type="password" id="password" name="password" v-model="input.password" placeholder="Пароль" />
            </label>
        </div>
        <button type="button" v-on:click="login()">Login</button>
    </div>
</template>

<script>
export default {
    name: 'Login',
    data() {
        return {
            input: {
                username: "",
                password: ""
            }
        }
    },
    methods: {
        login() {
            if (this.input.username != "" && this.input.password != "") {
                if (this.input.username == this.$parent.mockAccount.username && this.input.password == this.$parent.mockAccount.password) {
                    this.$emit("authenticated", true);
                    this.$router.replace({ name: "Secure" });
                } else {
                    console.log("The username and / or password is incorrect");
                }
            } else {
                console.log("A username and password must be present");
            }
        }
    }
}
</script>

<style>
.login {
    padding: 97px 197px;
    max-width: 1046px;
}

#login .form-inputs {
    padding-bottom: 10px;
}

.form-inputs {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    margin-bottom: 20px;
}

#login .form-inputs label {
    display: flex;
    padding-right: 10px;
}
</style>