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
          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown text="Register" right>
              <b-dropdown-item to="/">Entrprenuer</b-dropdown-item>
              <b-dropdown-item to="/">Funder</b-dropdown-item>
            </b-nav-item-dropdown>

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
      <b-sidebar id="sidebar-1" title="Sidebar" right backdrop shadow>
        <div class="px-3 py-2">
          <p>
            Cras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis
            in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.
          </p>
          <b-img src="https://picsum.photos/500/500/?image=54" fluid thumbnail></b-img>
        </div>
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
