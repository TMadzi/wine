<template>
  <div class='main'>
    <div class='form-container'>
      <b-link to="/">
        <b-img src="../assets/images/logo/logo.png" class="logo"></b-img>
      </b-link>
      <h3 class="login-header">Log In</h3>
      <b-form class="form" @submit="onSubmit">
      <b-form-group
          id="input-group-1"
          label-for="input-1"
          description="We'll never share your email with anyone else."
      >
          <b-form-input
          id="input-1"
          type="email"
          required
          v-model="form.email"
          placeholder="Enter email"
          ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label-for="input-2">
          <b-form-input
          id="input-2"
          type="password"
          v-model="form.password"
          required
          placeholder="Enter name"
          ></b-form-input>
      </b-form-group>
      <b-form-checkbox value="that">Keep me signed in</b-form-checkbox>
      <b-button type="submit" class="sign-in" >Login</b-button>
      <br>
      <b-link to="/register">Register now</b-link>
      </b-form>
    </div>
  </div>
</template>
<script>
import GoTrue from 'gotrue-js'
const auth = new GoTrue({
  APIUrl: 'https://uncorked.netlify.app/.netlify/identity',
  audience: '',
  setCookie: false
})
export default {
  data () {
    return {
      form: {
        email: '',
        password: ' '
      }
    }
  },
  transitions: 'home',
  layout: 'null',
  methods: {
    onSubmit (evt) {
      evt.preventDefault()
      const email = this.form.email
      const password = this.form.password
      console.log(this.form.passsword)
      console.log(this.form.email)
      // login existing user with a username and password
      auth
        .login(email, password, true)
        .then((response) => {
          alert('Success! Response: ' + JSON.stringify({ response }), this.form)
          console.log(email)
        })
        .catch(error => alert('Failed :( ' + JSON.stringify(error), this.form))
    }
  }
}
</script>
<style>
.home-enter-active, .home-leave-active { transition: opacity 1s; }
.home-enter, .home-leave-active { opacity: 0; }

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
  background: rgb(72, 35, 101);
  padding: 10px 30px;
  font-size: 1.3rem;
  margin: 30px 0;
  width: 100%;
  font-weight: 700;
  letter-spacing: .2em;
  line-height: .9;
  text-transform: uppercase;
  border: 1px solid rgb(72, 35, 101);
}
.sign-in:hover{
  color: rgb(72, 35, 101);;
  background: white;
  padding: 10px 30px;
  text-decoration: none;
}

.form{
  padding: 50px;
}
.hfrom-input{
  border-color:transparent;
  outline: 0;
  background-color: rgba(241, 241, 241, 0.644);
  transition: 300ms all ease;
}
.hfrom-input:focus{
  border-color:transparent;
  outline: 0;
  background-color: white;
  box-shadow: 0 0 0 0.2rem rgba(126, 5, 116, 0.25);
  transition: 300ms all ease;
}
  .contact-input::after{
    content: " ";
    height: 5px;
    display: block;
    width: 0%;
    background-color: rgb(72, 35, 101);
    transition: 300ms all ease;
  }
    .contact-input:focus-within:after{
    width: 100%;
    transition: 300ms all ease;
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
