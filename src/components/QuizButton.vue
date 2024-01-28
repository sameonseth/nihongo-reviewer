<template>
    <div
    v-for="(quizCode, index) in n5VocabularyCodeQuizArray"
    :key="quizCode"
    >
        <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz(quizCode)"
        >
        {{ n5FirstName + (index+1) + vocabularyOptionLastName }}
        </button>
    </div>
    <div
    v-for="(quizCode, index) in n4VocabularyCodeQuizArray"
    :key="quizCode"
    >
        <button
        type="button"
        class="vocabulary-option"
        @click.prevent="setQuiz(quizCode)"
        >
        {{ n4FirstName + (index+26) + vocabularyOptionLastName }}
        </button>
    </div>
    <div
    v-for="(quizCode, index) in n5KanjiCodeQuizArray"
    :key="quizCode"
    >
        <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz(quizCode)"
        >
        {{ n5FirstName + (index+1) + kanjiOptionLastName }}
        </button>
    </div>
    <div
    v-for="(quizCode, index) in n4KanjiCodeQuizArray"
    :key="quizCode"
    >
        <button
        type="button"
        class="kanji-option"
        @click.prevent="setQuiz(quizCode)"
        >
        {{ n4FirstName + (index+1) + kanjiOptionLastName }}
        </button>
    </div>
</template>
<script>
    export default {
        props: ["n4KanjiCodeQuizArray", "n4VocabularyCodeQuizArray", "n5KanjiCodeQuizArray", "n5VocabularyCodeQuizArray"],
        emits: ["setQuiz"],
        data() {
            return {
                kanjiOptionLastName: " Kanji",
                n4FirstName: "N4 L",
                n5FirstName: "N5 L",
                vocabularyOptionLastName: " Vocabulary"
            };
        },
        methods: {
            setQuiz(selectedQuiz){
                this.$emit("setQuiz", selectedQuiz);
            }
        }
    }
</script>