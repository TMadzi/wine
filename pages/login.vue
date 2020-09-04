<template>
  <div class='main'>
    <div class='form-container'>
      <h2>Oh So Cellar</h2>
      <h3 class="login-header">Log In</h3>
      <b-form class="form" @submit="onSubmit" @reset="onReset">
      <b-form-group
          id="input-group-1"
          label-for="input-1"
          description="We'll never share your email with anyone else."
      >
          <b-form-input
          id="input-1"
          type="email"
          required
          placeholder="Enter email"
          ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label-for="input-2">
          <b-form-input
          id="input-2"
          type="password"
          required
          placeholder="Enter name"
          ></b-form-input>
      </b-form-group>
      <b-form-checkbox value="that">Keep me signed in</b-form-checkbox>
      <b-button type="submit" class="sign-in" >Login</b-button>
      <br>
      <b-link to="/register-funder">Register now</b-link>
      </b-form>
    </div>
  </div>
</template>
<script>
export default {
  layout: 'null'
}
</script>
<style>
.main{
  background:rgb(240, 240, 245);
  height:100vh;
  padding: 2rem;
}
.form-container{
  padding: 3rem;
  text-align: center;
  background-color: rgb(244, 244, 250);
}
.form{
  padding-top:10px;
}
.sign-in{
  color: white;
  background: rgb(126, 5, 116);
  padding: 10px 30px;
  font-size: 1.3rem;
  margin: 30px 0;
  width: 100%;
  font-weight: 700;
  letter-spacing: .2em;
  line-height: .9;
  text-transform: uppercase;
  border: 1px solid rgb(126, 5, 116);
}
.sign-in:hover{
  color: rgb(126, 5, 116);;
  background: white;
  padding: 10px 30px;
  text-decoration: none;
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .main{
  background: url('../assets/images/wine2.jpg') center center / cover no-repeat fixed;
  padding: 3rem;
}
  .form-container{
  margin: 0 auto;
  max-width: 500px;
  min-height: 660px;
  padding: 3rem;
  text-align: center;
  background-color: rgba(244, 244, 250, 0.69);
  box-shadow: rgb(94, 105, 125) 0px 1px 5px 0px;
}
.login-header{
  margin-top: 40px;
  margin-bottom: 30px;
}
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {

}
/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {}
</style>
