<template>
  <div>
    <div class="top-section container-fluid p-0">
      <b-row no-gutters>
        <b-col class ='d-none d-md-block contact-bg'>
        </b-col>
        <b-col cols="12" md="6" class="contact-col">
          <h2 class="main-heading">
            We'd love to hear from you
          </h2>
          <p class="top-text">
            We are always striving to give our customers the best possible service. If you'd like to query, comment or voice a concern, please fill in the form below and we will get back to you as soon as possible.
          </p>
          <b-form class="form">
          <b-form-group
              id="name-group"
              label-for="name-group"
              class="contact-input"
          >
              <b-form-input
              id="first-name"
              class="hfrom-input"
              autocomplete="nnde"
              type="text"
              required
              placeholder="Name"
              ></b-form-input>
          </b-form-group>
          <b-form-group
              id="input-group-1"
              label-for="input-1"
              class="contact-input"
          >
              <b-form-input
              id="input-1"
              type="email"
              class="hfrom-input"
              autocomplete="nonse"
              required
              placeholder="Email Address"
              ></b-form-input>
          </b-form-group>
          <b-form-group
              id="number-group"
              label-for="number-group"
              class="contact-input"
          >
              <b-form-input
              id="Phone Number"
              autocomplete="htgt"
              class="hfrom-input"
              type="text"
              required
              placeholder="Phone Number"
              ></b-form-input>
          </b-form-group>
          <b-form-group id="input-group-2" label-for="input-2">
              <b-textarea
              id="message"
              type="text"
              class="hfrom-input"
              rows="5"
              required
              placeholder="Message"
              ></b-textarea>
          </b-form-group>
          <b-button type="submit" class="sign-in" >Submit</b-button>
          </b-form>

        </b-col>
      </b-row>
    </div>
  </div>
</template>
<script>
export default {
}
</script>
<style scoped>
.main-heading{
  color: #362d70;
  font-size: 3.5rem;
  width: 61%;
  margin: 0 auto 28px auto;
  text-transform: capitalize;
  font-weight: 700;
  line-height: 3.5rem;
  text-align: center;
}
.centered{
  text-align: center;
}

.top-text{
  text-align: center;
  width: 80%;
  margin: 10px auto 10px auto;
}
.start-btn{
  margin: 40px  0;
}

.sign-in{
  color: white;
  background: rgb(72, 35, 101);
  padding: 10px 30px;
  font-size: 1.3rem;
  margin: 10px 0;
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
.top-image{
  width: 100%;
}
.contact-bg{
  background: url('../assets/images/wine2.jpg');
  background-size: cover;
  background-position: center;
  height: calc(100vh-80px);
}

.contact-col{
      padding: 60px 60px 0 60px;
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
  /* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .top-container{
    height: calc(100vh - 80px);
  }
  .main-heading{
    font-size: 2.5rem;
    width: 100%;
  }
  .sign-in{
    margin-bottom:0;
  }
  .form{
    padding: 30px 50px 50px 50px;
  }
}
</style>
