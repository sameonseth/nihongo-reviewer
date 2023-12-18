<template>
    <button
    type="button"
    class="vocabulary-option"
    @click.prevent="setQuiz('N5L1VQuiz')"
    >
    N5 L1 Vocabulary
    </button>
</template>
<script>
    export default {
        props: ["buttonClass"],
        emits: ["setQuiz"],
        methods: {
            setQuiz(selectedQuiz){
                this.$emit("setQuiz", selectedQuiz);
            }
        }
    }
</script>