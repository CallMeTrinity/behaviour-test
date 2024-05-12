<template>
  <div>
    <p>{{ question.question }}</p>
    <select v-model="question.score">
      <option value="0">0 - Pas du tout moi / Jamais</option>
      <option value="1">1 - Ça peut m'arriver / Parfois</option>
      <option value="2">2 - Ça me ressemble / Souvent</option>
      <option value="3">3 - Tout à fait moi / Toujours</option>
    </select>
  </div>
</template>

<script>
export default {
  props: {
    question: Object,
    required: true
  }
}
</script>
