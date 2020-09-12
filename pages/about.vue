<template>
  <div>
    <div class="top-section container">
      <h2 class="main-heading">
        There's nothing like a fine wine
      </h2>
      <p class="top-text">
        Oh So Cellar is a new Zimbabwean wine club that matches you with wines that we know you will love.
      </p>
      <p class="top-text">
        Take our wine quiz and we will provide you with personalized matches.
      </p>
      <p class="centered start-btn">
        <b-link class="start-button">Get Started</b-link>
      </p>
    </div>
  </div>
</template>
<script>
export default {
  transition: 'home'
}
</script>
<style scoped>
.home-enter-active, .home-leave-active { transition: opacity 1s; }
.home-enter, .home-leave-active { opacity: 0; }

.main-heading{
  color: #362d70;
  font-size: 2.5rem;
  margin: 0 auto 28px auto;
  text-transform: capitalize;
  font-weight: 700;
  line-height: 3.5rem;
  text-align: center;
}
.centered{
  text-align: center;
}
.steps{
  margin-bottom: 40px;
}
.top-text{
  text-align: center;
  width: 80%;
  margin: 10px auto 10px auto;
}
.start-btn{
  margin: 40px  0;
}

.start-button{
  color: white;
  background: rgb(72, 35, 101);
  padding: 10px 30px;
  font-size: 1.3rem;
  font-weight: 700;
  letter-spacing: .2em;
  line-height: .9;
  text-transform: uppercase;
  border: 1px solid rgb(72, 35, 101);
  transition: all 600ms ease;
}
.start-button:hover{
  color: rgb(72, 35, 101);
  background: white;
  padding: 10px 30px;
  text-decoration: none;
  transition: all 600ms ease;
}
.top-image{
  width: 100%;
}
</style>
