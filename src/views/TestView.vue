<template>
  <div>
    <h1>Test de Personnalité</h1>
    <form @submit.prevent="submitAnswers">
      <Question v-for="(question, index) in questions" :key="question.id" :question="question" />
      <button type="submit">Soumettre les réponses</button>
    </form>
  </div>
</template>

<script>
import Question from '../components/Question.vue';
import questions from '../data/question.js';

export default {
  components: {
    Question
  },
  data() {
    return {
      questions
    };
  },
  methods: {
    submitAnswers() {
      console.log("Réponses soumises:", this.questions);
      // Ajouter ici la logique pour traiter ou envoyer les réponses
    }
  }
}
</script>
