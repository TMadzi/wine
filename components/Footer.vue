<template>
  <footer>
    <div class="social">
      <p class="our-social">Connect</p>
      <b-link class="social-link"><i class="fas abacus"></i></b-link>
      <b-link class="social-link">INSTA</b-link>
      <b-link class="social-link">TWITTER</b-link>
    </div>
      <div class="social">
      <p class="our-social">Contact</p>
      <b-link class="contact-link">+263771417667</b-link>
      <b-link class="contact-link">sales@uncorked.co.zw</b-link>
    </div>

  </footer>
</template>
<style>
  footer{
    height:30vh;
    background: #362d70;
    padding: 35px 40px;
  }
  .social{
    text-align: center;
    padding-bottom:20px;
  }
  .our-social{
    color: rgba(255, 255, 255, 0.808);
    font-size:18px;
    font-weight:bold;
    text-align: center;
    font-size:18px;
  }
  .social-link{
    display:inline-block
  }
  .contact-link{
    display:block;
    color: rgba(255, 255, 255, 0.808);
  }
  .contact-link:hover{
    text-decoration: none;
    color:white;
  }
</style>
