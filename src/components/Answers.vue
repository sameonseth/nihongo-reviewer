<template>
  <div class="items-container">
    <transition-group name="fade">
      <div
        class="single-item"
        v-for="(quizItem, loopIndex) in quiz"
        :key="quizItem.question"
      >
        <div class="question">{{ quizItem.question }}</div>
        <div 
          v-if="userAnswerArray[loopIndex] === quizItem.answer"
          class="answer"
        >
          {{ quizItem.answer }}
        </div>
        <div v-else class="answer-danger">
          {{ userAnswerArray[loopIndex] }}
          <span class="correct-answer"> ({{ quizItem.answer }}) </span>
        </div>
        <div v-if="typeOfQuiz === 'kanji'">
          <div 
            v-if="userEnglishAnswerArray[loopIndex] === quizItem.english_answer.toLowerCase()"
            class="answer"
          >
            {{ quizItem.english_answer }}
          </div>
          <div v-else class="answer-danger">
            {{ userEnglishAnswerArray[loopIndex] }}
            <span class="correct-answer"> ({{ quizItem.english_answer }}) </span>
          </div>
        </div>
      </div>
    </transition-group>
  </div>
</template>

<script>
export default {
  props: ["quiz", "typeOfQuiz", "userAnswerArray", "userEnglishAnswerArray"],
};
</script>
