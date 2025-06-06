<template>
    <div>
      <h2>Home Page</h2>
      <p>Welcome to the home page!</p>
      
      <!-- About 페이지로 이동하는 링크 -->
      <router-link to="/about">Go to About Page</router-link> <!-- Vue Router를 이용해 이동 -->
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomePage'  // 컴포넌트 이름
  }
  </script>
  
  <style scoped>
  /* 스타일 정의 */
  </style>
  