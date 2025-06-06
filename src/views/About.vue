<template>
  <div>
    <h2>About Page</h2>
    <p v-if="text">You entered: {{ text }}</p>
    <p v-else>No text entered</p>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  computed: {
    // URL에서 쿼리 파라미터 'text'를 읽어옵니다.
    text() {
      return this.$route.query.text; // 쿼리 파라미터로 전달된 'text'
    },
  },
};
</script>
