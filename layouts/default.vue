<template>
  <div>
    <div class="navi">
      <b-navbar toggleable="lg">
        <b-navbar-brand href="#">Oh So Cellar</b-navbar-brand>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item to="/login">Login</b-nav-item>
            <b-nav-item to="/">About</b-nav-item>
            <b-nav-item to="/">Contact</b-nav-item>
          </b-navbar-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav>
            <b-nav-item to="/register">Register</b-nav-item>
            <b-nav-item to="/login">Sign In</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
        <div class="mobile-sidebar-nav">
      <b-button class="sidebar-toggle" v-b-toggle.sidebar-1>
          <span class="header-bars">
            <span></span>
            <span></span>
            <span></span>
          </span>
      </b-button>
      <b-sidebar id="sidebar-1" class="menu-sidebar"  right backdrop shadow>
        <div class="sidebar-btn-cont">
          <b-link to="/register" class="siderbar-btn reg">Register</b-link>
          <b-link to="/login" class="siderbar-btn sign">Sign In</b-link>
        </div>
        <b-link to="/" class="sidebar-menu-item">Home</b-link>
        <b-link to="/about" class="sidebar-menu-item">About Us</b-link>
        <b-link to="/contact" class="sidebar-menu-item">Contact Us</b-link>
      </b-sidebar>
    </div>
      </b-navbar>
    </div>
      <Nuxt />
      <Footer />
  </div>
</template>
<script>
import Footer from '~/components/Footer.vue'
export default {
  components: {
    Footer
  }
}
</script>
<style>
.navi{
  border-bottom: 1px solid rgb(243, 229, 229);
  padding-bottom:10px;
}
.sidebar-toggle{
  border-color: white;
  background-color: white;;
}
.sidebar-btn-cont{
  text-align: center;
  margin: 0 auto 40px auto;
}
.siderbar-btn {
  border: 1px solid rgb(126, 5, 116);
  padding: 5px 20px;
  color: rgb(126, 5, 116);
  text-transform: uppercase;
}
.reg{
  color: white;
  background-color: rgb(126, 5, 116);
  transition: all 600ms ease;
  margin-right:10px;
}
.reg:hover{
  font-size:18px;
  padding: 3.5px 15px;
  text-decoration: none;
  color: white;
  transition: all 600ms ease;
}
.sign{
  background-color: white;
  color: rgb(126, 5, 116);
  transition: all 600ms ease;
  margin-left:10px;
}
.sign:hover{
  font-size:18px;
  padding: 3.5px 15px;
  text-decoration: none;
  color: rgb(126, 5, 116);
  transition: all 600ms ease;
}
.b-sidebar-body{
  padding: 20px 30px;
}
.sidebar-menu-item{
  display:block;
  font-size:24px;
  padding:10px;
  color:rgb(77, 77, 77);
}
.sidebar-menu-item:hover{
text-decoration: none;
color: rgb(126, 5, 116);
}
.sidebar-toggle:hover{
  border-color: rgb(126, 5, 116);
  background-color: white;;
}
.sidebar-toggle:active{
  border-color: white;
  background-color: white;;
}
.sidebar-toggle:focus{
  border-color: white;
  background-color: white;;
}
.header-bars{
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  padding-bottom:1.1em;
  display: block;
  height: .75em;
  position: relative;
  width: 1.1em;
}
.header-bars>span{
  background:rgb(126, 5, 116);
  border-radius: .1em;
  display: block;
  -ms-flex-negative: 0;
  flex-shrink: 0;
  height: .2em;
  -webkit-transition: all .25s;
  margin:3px 0;
  transition: all .25s;
  width: 100%;
}
.navbar-light .navbar-toggler {
  color: rgba(0, 0, 0, 0.5);
  border-color: transparent;
}
/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .mobile-sidebar-nav{
    display: none;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {}
</style>
