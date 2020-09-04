<template>
  <div>
    <div class="navi">
      <b-navbar toggleable="lg">
        <b-navbar-brand href="#">Oh So Cellar</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse">
          <span class="header-bars">
            <span></span>
            <span></span>
            <span></span>
          </span>
        </b-navbar-toggle>

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
  background:rgb(126, 5, 116);;
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
</style>
