<template>
    <div class="heading-card">
        <div class="heading-card-title">こんにちは！</div>
        <div class="heading-card-description">
            Please choose what type of quiz you want to take.
            <div class="text-danger margin-top-1">
                *Note: This app follows みんなの日本語 book's vocabularies and kanjis for each lesson.
            </div>
            <div class="text-danger">
                **Note: Answers that includes ～, 「, ［, 。, 、, or even just whitespace might be marked wrong.
            </div>
        </div>
    </div>
    <div class="grid-container short">
      <QuizButton :buttonClass="buttonClass" @setQuiz="setQuiz"/>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L2VQuiz')"
      >
        N5 L2 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L3VQuiz')"
      >
        N5 L3 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L4VQuiz')"
      >
        N5 L4 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L5VQuiz')"
      >
        N5 L5 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L6VQuiz')"
      >
        N5 L6 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L7VQuiz')"
      >
        N5 L7 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L8VQuiz')"
      >
        N5 L8 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L9VQuiz')"
      >
        N5 L9 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L10VQuiz')"
      >
        N5 L10 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L11VQuiz')"
      >
        N5 L11 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L12VQuiz')"
      >
        N5 L12 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L13VQuiz')"
      >
        N5 L13 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L14VQuiz')"
      >
        N5 L14 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L15VQuiz')"
      >
        N5 L15 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L16VQuiz')"
      >
        N5 L16 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L17VQuiz')"
      >
        N5 L17 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L18VQuiz')"
      >
        N5 L18 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L19VQuiz')"
      >
        N5 L19 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L20VQuiz')"
      >
        N5 L20 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L21VQuiz')"
      >
        N5 L21 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L22VQuiz')"
      >
        N5 L22 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L23VQuiz')"
      >
        N5 L23 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L24VQuiz')"
      >
        N5 L24 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L25VQuiz')"
      >
        N5 L25 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L26VQuiz')"
      >
        N4 L26 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L27VQuiz')"
      >
        N4 L27 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L28VQuiz')"
      >
        N4 L28 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L29VQuiz')"
      >
        N4 L29 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L30VQuiz')"
      >
        N4 L30 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L31VQuiz')"
      >
        N4 L31 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L32VQuiz')"
      >
        N4 L32 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L33VQuiz')"
      >
        N4 L33 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L34VQuiz')"
      >
        N4 L34 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L35VQuiz')"
      >
        N4 L35 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L36VQuiz')"
      >
        N4 L36 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L37VQuiz')"
      >
        N4 L37 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L38VQuiz')"
      >
        N4 L38 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L39VQuiz')"
      >
        N4 L39 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L40VQuiz')"
      >
        N4 L40 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L41VQuiz')"
      >
        N4 L41 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N4L42VQuiz')"
      >
        N4 L42 Vocabulary
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L1KQuiz')"
      >
        N5 L1 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L2KQuiz')"
      >
        N5 L2 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L3KQuiz')"
      >
        N5 L3 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L4KQuiz')"
      >
        N5 L4 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L5KQuiz')"
      >
        N5 L5 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L6KQuiz')"
      >
        N5 L6 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L7KQuiz')"
      >
        N5 L7 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N5L8KQuiz')"
      >
        N5 L8 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L1KQuiz')"
      >
        N4 L1 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L2KQuiz')"
      >
        N4 L2 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L3KQuiz')"
      >
        N4 L3 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L4KQuiz')"
      >
        N4 L4 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L5KQuiz')"
      >
        N4 L5 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L6KQuiz')"
      >
        N4 L6 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L7KQuiz')"
      >
        N4 L7 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L8KQuiz')"
      >
        N4 L8 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L9KQuiz')"
      >
        N4 L9 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L10KQuiz')"
      >
        N4 L10 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L11KQuiz')"
      >
        N4 L11 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L12KQuiz')"
      >
        N4 L12 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L13KQuiz')"
      >
        N4 L13 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('N4L14KQuiz')"
      >
        N4 L14 Kanji
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('NextKQuiz')"
      >
        Next Kanji Quiz
      </button>
      <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz('NextNextKQuiz')"
      >
        Next Next Kanji Quiz
      </button>
      <button
        type="button"
        class="script-option"
        @click.prevent="setQuiz('OQ2')"
      >
        Oral 2 Script Questions
      </button>
    </div>
</template>

<script>
  import QuizButton from "./QuizButton.vue";
  export default {
    components: {
      QuizButton
    },
    data() {
      return {
        buttonClass: "vocabulary-option"
      };
    },
    emits: ["setQuiz"],
    methods: {   
        setQuiz(selectedQuiz){
            this.$emit("setQuiz", selectedQuiz);
        }
    }
  };
</script>