<template>
  <div>
    <b-container class="wine-quiz">
        <div v-for='question in lquiz.questions' :key='question.questionIndex'>
          <transition
            name="custom-classes-transition"
            enter-active-class="animated tada"
            leave-active-class="animated bounceOutRight"
          >
          <div v-show='index === question.questionIndex' key = question.questionIndex>
            <h2 class="question-text">{{ question.questionTitle }}</h2>
            <div v-if='question.questionType === "imageQ" '>
              <b-row>
                  <b-col
                    class="question-col"
                    v-on:click ="nextQuestion(response.id)"
                    v-for='response in question.responses'
                    :key='response.id'
                    cols="12"
                    md="6"
                  >
                    <b-card
                    :title= response.responseText
                    :img-src= response.imageSrc
                    img-alt="Image"
                    img-top
                    class="image-question quiz-col">
                    </b-card>
                  </b-col>
              </b-row>
            </div>
            <div v-else>
              <b-row no-gutters>
                <b-col v-on:click ="nextQuestion(response.id)" v-for='response in question.responses' :key='response.id' cols="12">
                  <b-card class="text-question quiz-col">{{ response.responseText }}</b-card>
                </b-col>
              </b-row>
            </div>
          </div>
          </transition>
        </div>
      <div class="movement-btns">
        <b-link v-show="index > 0 && index < 11" v-on:click ="previousQuestion" class="step-btn-p previous-btn">PREVIOUS</b-link>
        <b-link v-if="index == 11" @:click ="sumbitQuestions" class="step-btn-p previous-btn">SUBMIT</b-link>
      </div>
    </b-container>
  </div>
</template>
<script>
import faunadb, { query as q } from 'faunadb'

const serverClient = new faunadb.Client({ secret: 'fnAD1ZCo9PACBQSVCOxDVPBMS7DVDWZktiio7ajv' })

export default {
  transition: 'home',
  data () {
    return {
      lquiz: [],
      // Store current question index
      index: 0,
      // Empty array of the users answers
      userResponses: []
    }
  },
  async fetch () {
    this.lquiz = await serverClient.query(
      q.Get(q.Ref(q.Collection('quiz'), '276287450835321345'))
    )
      .then(res => res.data)
    console.log(this.lquiz)
  },
  methods: {
    previousQuestion () {
      this.index--
      this.userResponses.pop()
    },
    nextQuestion (id) {
      this.userResponses.push(this.lquiz.questions[this.index].responses[id].responseText)
      this.index++
    },
    submitQuestions (id) {
      this.userResponses.push(this.lquiz.questions[this.index].responses[id].responseText)
      this.index++
    }
  }
}
</script>
<style>
.home-enter-active, .home-leave-active { transition: opacity 1s; }
.home-enter, .home-leave-active { opacity: 0; }

  .wine-quiz{
    padding: 60px 0;
  }
  .quiz-intro{
    text-align: center;
  }
  .question{
    text-align: center;
    font-size: 1.8rem;
    color: #2f2e2e;
  }
  .question-div{
    transition: opacity 300ms ease;
  }
  .question-col{
    padding: 0 25%;
  }
  .question-text{
    text-align: center;
  }
  .quiz-col{
    padding:2px;
    margin-bottom: 20px;
  }
  .card-title{
    text-align: center;
    font-size: 1.2em;
  }
.text-question{
  margin: 10px auto;
        -webkit-box-shadow: inset 0 0 0 2px rgba(255, 255, 255, 0.75), 2px 4px 7px rgba(0,0,0,.15);
    box-shadow: inset 0 0 0 2px rgba(255, 255, 255, 0.75), 2px 4px 7px rgba(0,0,0,.15);
}
.image-question{
      -webkit-box-shadow: inset 0 0 0 2px rgba(255, 255, 255, 0.75), 2px 4px 7px rgba(0,0,0,.15);
    box-shadow: inset 0 0 0 2px rgba(255, 255, 255, 0.75), 2px 4px 7px rgba(0,0,0,.15);
    transition: 400ms all ease;
}
.image-question .card-img, .card-img-top, .card-img-bottom {
    width: 100%;
    margin: 0 auto;
    text-align: center;
}
.quiz-col:hover{
    -webkit-box-shadow: inset 0 0 0 2px rgb(72, 35, 101), 2px 4px 7px rgba(0,0,0,.15);
    box-shadow: inset 0 0 0 2px rgb(72, 35, 101), 2px 4px 7px rgba(0,0,0,.15);
    cursor: pointer;
    transition: 400ms all ease;
}
.card-body{
    padding: .75rem;
}
.movement-btns{
  margin-top: 25px;
}
.step-btn-p{
  padding: 15px;
  color: white;
  background-color: rgb(72, 35, 101);
  margin-right: 20px;
  width: 100px;
  border: 1px solid rgb(72, 35, 101);
  transition: 300ms all ease;
}
.step-btn-n{
  padding: 15px 35px;
  color: white;
  background-color: rgb(72, 35, 101);
  width: 100px;
  border: 1px solid rgb(72, 35, 101);
  transition: 300ms all ease;
}
.step-btn-p:hover{
  color: rgb(72, 35, 101);
  background-color: white;
  transition: 300ms all ease;
  text-decoration: none;
}
.step-btn-n:hover{
  color: rgb(72, 35, 101);
  background-color: white;
  transition: 300ms all ease;
  text-decoration: none;
}
/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
    .question-col{
    padding: 2px 12%;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .wine-quiz{
  padding: 30px 10%;
}
}
/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {}
</style>
