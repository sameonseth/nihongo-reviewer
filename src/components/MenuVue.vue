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
    <div class="grid-container">
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L1V')"
      >
        N5 L1 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L2V')"
      >
        N5 L2 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L3V')"
      >
        N5 L3 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L4V')"
      >
        N5 L4 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L5V')"
      >
        N5 L5 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L6V')"
      >
        N5 L6 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L7V')"
      >
        N5 L7 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L8V')"
      >
        N5 L8 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L9V')"
      >
        N5 L9 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L10V')"
      >
        N5 L10 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L11V')"
      >
        N5 L11 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L12V')"
      >
        N5 L12 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L13V')"
      >
        N5 L13 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L14V')"
      >
        N5 L14 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L15V')"
      >
        N5 L15 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L16V')"
      >
        N5 L16 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L17V')"
      >
        N5 L17 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L18V')"
      >
        N5 L18 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L19V')"
      >
        N5 L19 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L20V')"
      >
        N5 L20 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L21V')"
      >
        N5 L21 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L22V')"
      >
        N5 L22 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L23V')"
      >
        N5 L23 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L24V')"
      >
        N5 L24 Vocabulary
      </button>
      <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz('N5L25V')"
      >
        N5 L25 Vocabulary
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
        @click.prevent="setQuiz('NextKanjiQuiz')"
      >
        Next Kanji Quiz
      </button>
    </div>
</template>

<script>
    export default {
        emits: ["setQuiz"],
        methods: {   
            setQuiz(selectedQuiz){
                this.$emit("setQuiz", selectedQuiz);
            }
        }
    };
</script>