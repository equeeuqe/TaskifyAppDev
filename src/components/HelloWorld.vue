<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button id="SignUp"><router-link to="/SignUp">Sign Up</router-link></button>
    <button id="LogIn"><router-link to="/LogIn">Log In</router-link></button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  font-size: 100px;
}

#SignUp {
  margin-top: 30px;
  margin-right: 50px;
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
  transition-duration: 0.4s;
  border-radius: 12px;
  font-size: 16px;
  padding: 15px 25px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: black;
}

#SignUp:hover {
  background-color: #FAD744; 
  color: white;
}

#LogIn {
  margin-top: 30px;
  margin-left: 50px;
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
  transition-duration: 0.4s;
  border-radius: 12px;
  font-size: 16px;
  padding: 15px 25px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}

#LogIn:hover{
  background-color:#ef5455; /* Green */
  color: white;
}

</style>
