<template>
  <div>
    <div class="top-section container">
      <h2 class="main-heading">
        Discover your wine experience
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
    <div class="header-background">
      <div class="top-section-lg container">
        <h2 class="main-heading">
          Discover your wine experience
        </h2>
        <p class="top-text">
          Oh So Cellar is a new Zimbabwean wine club that matches you with wines that we know you will love.
        </p>
        <p class="top-text">
          Take our wine quiz and we will provide you with personalized matches.
        </p>
        <p class="centered start-btn start-btn-lg">
          <b-link class="start-button">Get Started</b-link>
        </p>
      </div>
    </div>
    <div class="how-it-works">
      <h2 class="how-heading">
        How we work
      </h2>
      <b-row>
        <b-col cols='12' md='4' class="centered">
          <b-img class="how-image" src="../assets/images/1.png"></b-img>
          <h3 class="how-step-heading">Take Our Quiz</h3>
          <p>Take our quiz and get your unique wine profile</p>
        </b-col>
        <b-col cols='12' md='4' class="centered">
          <b-img class="how-image" src="../assets/images/2.png"></b-img>
          <h3 class="how-step-heading">View Matches</h3>
          <p>Take our quiz and get your unique wine profile</p>
        </b-col>
        <b-col cols='12' md='4' class="centered">
          <b-img class="how-image" src="../assets/images/3.png"></b-img>
          <h3 class="how-step-heading">Enjoy</h3>
          <p>Take our quiz and get your unique wine profile</p>
        </b-col>
      </b-row>
      <p class="centered start-btn">
        <b-link class="start-button">Sign Me Up</b-link>
      </p>
    </div>
    <div class="cta">
      <b-row>
        <b-col class="cta-col"></b-col>
      </b-row>
    </div>
    <div>
      <b-row>
        <b-col cols="12" md="6">
          <b-img src="../assets/images/wine2.jpg" class="top-image" alt="Fluid image"></b-img>
        </b-col>
        <b-col cols="12" md="6">
        <div class="how-it-works">
          <h2 class="curated-heading">
            Specially Curated For Your Pleasure
          </h2>
          <p class="cellar-text">
            We specially curated a list of wines from across the world for you to enjoy.
            We are fully confident that you will love the wines that we get for you and if you would like to
            specifically order a wine that you love, don't hesitate to buy from us.
          </p>
          <p class="centered start-btn">
          <b-link class="start-button">I'm Ready</b-link>
          </p>
        </div>
        </b-col>
      </b-row>
  </div>
  </div>
</template>
<script>
export default {}
</script>

<style>
.top-section{
  padding: 20px 0 10px 0;
}
.top-section-lg{
  display:none;
}
.main-heading{
  color: #0f4e63;
  font-size: 2.15rem;
  width:40%;
  margin: 0 auto;
  text-transform: capitalize;
  font-weight: 700;
  line-height: 2.8rem;
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
.start-button{
  color: white;
  background: rgb(126, 5, 116);
  padding: 10px 30px;
  font-size: 1.3rem;
  font-weight: 700;
  letter-spacing: .2em;
  line-height: .9;
  text-transform: uppercase;
  border: 1px solid rgb(126, 5, 116);
}
.start-button:hover{
  color: rgb(126, 5, 116);;
  background: white;
  padding: 10px 30px;
  text-decoration: none;
}
.top-image{
  width: 100%;
}
.how-heading{
  color: #0f4e63;
  font-size: 1.8rem;
  margin: 0 auto;
  text-transform: capitalize;
  padding: 24px 36px;
  font-weight: 700;
  line-height: 2.8rem;
  text-align: center;
}
.how-image{
  width:40%;
  margin: 0 auto;
  text-align: center;
}
.how-step-heading{
  color: #0f4e63;
  font-size: 1.5rem;
}
.header-background{
  background: url('../assets/images/wine1.jpg') center center / cover no-repeat fixed;
  height: 400px;
}
.curated-heading{
  color: #0f4e63;
  font-size: 1.8rem;
  margin: 0 auto;
  width:70%;
  text-transform: capitalize;
  padding: 24px 36px 0px 36px;
  font-weight: 700;
  line-height: 2.8rem;
  text-align: center;
}
.cellar-text{
  text-align: center;
  width: 70%;
  margin: 10px auto 10px auto;
}
.cta{
  height: 300px;
  background: #0f4e63;
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .main-heading{
    text-align:left;
    width: 90%;
  }
  .how-heading{
    font-size: 3rem;
    line-height: 3.563rem;
}
  .how-it-works{
      padding: 40px 0;
    }
  .curated-heading{
    padding-top:60px;
  }
  .curated-heading{
    font-size: 3rem;
    line-height: 3.563rem;
  }
  .top-section{
    display:none;
  }
  .top-section-lg{
    display:block;
    background: #f7f7f7;;
    padding: 20px;
    width:40%;
    border-radius: 30px;
    position:absolute;
    top:200px;
    left: 100px;
  }

.start-btn-lg {
    margin: 40px 26px;
    text-align: left;
}
  .top-text{
    text-align: left;
    width: 90%;
  }
  .header-background{
    background: url('../assets/images/wine1.jpg') center center / cover no-repeat fixed;
    height: 75vh;
  }

}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {}
</style>
