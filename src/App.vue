<template>
  <div class="container">
    <MenuVue 
      v-if="isQuizSelected === 0"
      @setQuiz="setQuiz"
    />
    <div v-else-if="isQuizSelected === 1">
      <transition name="fade" mode="out-in">
        <Questions
          v-if="numberOfAnsweredQuestions < totalNumberOfQuestions"
          :numberOfAnsweredQuestions="numberOfAnsweredQuestions"
          :quiz="quiz"
          :totalNumberOfQuestions="totalNumberOfQuestions"
          :typeOfQuiz="typeOfQuiz"
          @updateCounterVariables="updateCounterVariables"
          @updateUserAnswerArray="updateUserAnswerArray"
          @updateUserEnglishAnswerArray="updateUserEnglishAnswerArray"
        />
        <div v-else-if="numberOfAnsweredQuestions === totalNumberOfQuestions">
          <Result
            :numberOfCorrectAnswers="numberOfCorrectAnswers"
            :totalNumberOfQuestions="totalNumberOfQuestions"
          />  
          <Answers  
            v-if="isViewingAnswers === 1"
            :quiz="quiz"
            :typeOfQuiz="typeOfQuiz"
            :userAnswerArray="userAnswerArray"
            :userEnglishAnswerArray="userEnglishAnswerArray"
          />
        </div>
      </transition>
    </div>
    <button
      v-if="numberOfAnsweredQuestions < totalNumberOfQuestions"
      type="button"
      class="red-button"
      @click.prevent="skip"
    >
      Give Up
    </button>
    <div v-if="numberOfAnsweredQuestions === totalNumberOfQuestions">
      <button
        v-if="isViewingAnswers === 0"
        type="button"
        class="view-answers-button"
        @click.prevent="viewAnswers"
      >
        View Answers
      </button>
      <button
        type="button"
        class="red-button"
        @click.prevent="reset"
      >
        Take More Quizzes
      </button>
    </div>
  </div>
</template>

<script>
import N4KanjiQuizzes from "./assets/N4KanjiQuizzes.json";
import N5VocabularyQuizzes from "./assets/N5VocabularyQuizzes.json";
import Answers from "./components/Answers.vue";
import MenuVue from "./components/MenuVue.vue";
import Questions from "./components/Questions.vue";
import Result from "./components/Result.vue";

export default {
  name: "App",
  components: {
    Answers,
    MenuVue,
    Questions,
    Result
},
  data() {
    return {
      isQuizSelected: 0,
      isViewingAnswers: 0,
      numberOfAnsweredQuestions: 0,
      numberOfCorrectAnswers: 0,
      questionsIndexes: [],
      quiz: [],
      randomNum: 0,
      totalNumberOfQuestions: -1,
      typeOfQuiz: "",
      userAnswerArray: [],
      userEnglishAnswerArray: []
    };
  },
  methods: {
    generateRandomNumbers() {
      this.randomNum = Math.floor(Math.random() * this.totalNumberOfQuestions);
      if (this.questionsIndexes.indexOf(this.randomNum) === -1) {
        this.questionsIndexes.push(this.randomNum);
      } else {
        this.generateRandomNumbers();
      }
    },
    randomizeQuestions(questionSet){
      let randomizedQuestionSet = [];
      for(let i=0; i < questionSet.length; i++){
        this.generateRandomNumbers();
        randomizedQuestionSet[i] = questionSet[this.questionsIndexes[i]];
      }
      return randomizedQuestionSet;
    },
    reset() {
      this.isQuizSelected = 0;
      this.isViewingAnswers = 0;
      this.numberOfAnsweredQuestions = 0;
      this.numberOfCorrectAnswers = 0;
      this.questionsIndexes = [];
      this.quiz = [];
      this.randomNum = 0;
      this.totalNumberOfQuestions = -1;
      this.userAnswerArray = [];
      this.userEnglishAnswerArray = [];
    },
    updateCounterVariables(answer) {
      if (answer) {
        this.numberOfCorrectAnswers++;
      }
      this.numberOfAnsweredQuestions++;
    },
    setQuiz(selectedQuiz){
      this.isQuizSelected = 1;
      if (selectedQuiz==="N5L1V") {
        this.quiz = N5VocabularyQuizzes.N5L1VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L2V") {
        this.quiz = N5VocabularyQuizzes.N5L2VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L3V") {
        this.quiz = N5VocabularyQuizzes.N5L3VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L4V") {
        this.quiz = N5VocabularyQuizzes.N5L4VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L5V") {
        this.quiz = N5VocabularyQuizzes.N5L5VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L6V") {
        this.quiz = N5VocabularyQuizzes.N5L6VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L7V") {
        this.quiz = N5VocabularyQuizzes.N5L7VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L8V") {
        this.quiz = N5VocabularyQuizzes.N5L8VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L9V") {
        this.quiz = N5VocabularyQuizzes.N5L9VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L10V") {
        this.quiz = N5VocabularyQuizzes.N5L10VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L11V") {
        this.quiz = N5VocabularyQuizzes.N5L11VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L12V") {
        this.quiz = N5VocabularyQuizzes.N5L12VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L13V") {
        this.quiz = N5VocabularyQuizzes.N5L13VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L14V") {
        this.quiz = N5VocabularyQuizzes.N5L14VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L15V") {
        this.quiz = N5VocabularyQuizzes.N5L15VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L16V") {
        this.quiz = N5VocabularyQuizzes.N5L16VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L17V") {
        this.quiz = N5VocabularyQuizzes.N5L17VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L18V") {
        this.quiz = N5VocabularyQuizzes.N5L18VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L19V") {
        this.quiz = N5VocabularyQuizzes.N5L19VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L20V") {
        this.quiz = N5VocabularyQuizzes.N5L20VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L21V") {
        this.quiz = N5VocabularyQuizzes.N5L21VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L22V") {
        this.quiz = N5VocabularyQuizzes.N5L22VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L23V") {
        this.quiz = N5VocabularyQuizzes.N5L23VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L24V") {
        this.quiz = N5VocabularyQuizzes.N5L24VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="N5L25V") {
        this.quiz = N5VocabularyQuizzes.N5L25VQuiz;
        this.typeOfQuiz = "vocabulary";
      }
      else if (selectedQuiz==="UpcomingKQuiz") {
        this.quiz = N4KanjiQuizzes.UpcomingKQuiz;
        this.typeOfQuiz = "kanji";
      }
      this.totalNumberOfQuestions = this.quiz.length;
      this.quiz = this.randomizeQuestions(this.quiz);
    },
    updateUserAnswerArray(answer) {
      this.userAnswerArray.push(answer);
    },
    updateUserEnglishAnswerArray(answer) {
      this.userEnglishAnswerArray.push(answer);
    },
    viewAnswers() {
      this.isViewingAnswers = 1;
    },
    skip(){
      this.numberOfAnsweredQuestions = this.totalNumberOfQuestions;
    }
  },
};
</script>