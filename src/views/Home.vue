<template>
  <div>
    <h2>Home Page</h2>
    <input type="text" v-model="userInput" placeholder="Enter some text" />
    <button @click="goToAbout">Go to About Page</button>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      userInput: '', // 사용자가 입력한 텍스트
    };
  },
  methods: {
    goToAbout() {
      // 입력된 텍스트를 쿼리 파라미터로 전달
      this.$router.push({ path: '/about', query: { text: this.userInput } });
    },
  },
};
</script>
