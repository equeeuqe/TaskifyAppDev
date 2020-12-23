<template>
  <div id="login">
    <br><br>
    <h1>Login to your account</h1> <br>
    <input type="text" name="username" v-model="input.username" placeholder="Enter Username" /> <br><br>
    <input type="password" name="password" v-model="input.password" placeholder="Enter Password" /><br><br><br>
    <button type="button" v-on:click="login()">Log In!</button>
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
                if(this.input.username != "" && this.input.password != "") {
                    if(this.input.username == this.$parent.mockAccount.username && this.input.password == this.$parent.mockAccount.password) {
                        this.$emit("authenticated", true);
                        this.$router.replace({ name: "secure" });
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

<style scoped>
  #login {
        width: 450px;
        height: 400px;
        border: 10px solid #2b3252;
        background-color: #FFFFFF;
        margin: auto;
        /* margin-top: 1px; */
        padding: 20px;
        background-color:  #FAD744;
  }

  input[type=text] {
    width: 350px;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
    border-radius: 12px;
  }

  input[type=password] {
    width: 350px;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
    border-radius: 12px;
  }

  button[type=button] {
    width: 75px;
    height: 40px;
    margin: 8px 0;
    border-radius: 12px;
  }

  button[type=button]:hover {
        background-color: #ef5455; 
        color: white;
    }
</style>