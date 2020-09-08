<template>
  <div>
    <div class="top-section container">
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
    </div>
  </div>
</template>
<style>
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
    background-color: rgb(126, 5, 116);
    transition: 300ms all ease;
  }
    .contact-input:focus-within:after{
    width: 100%;
    transition: 300ms all ease;
  }

</style>
