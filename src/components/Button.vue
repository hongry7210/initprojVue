<template>
    <button
      :class="['btn', `btn-${type}`, { 'btn-disabled': disabled }]"
      :disabled="disabled"
      @click="handleClick"
    >
      <slot></slot> <!-- 버튼의 내용은 부모 컴포넌트에서 제공 -->
    </button>
  </template>
  
  <script>
  export default {
    name: 'BaseButton', // 컴포넌트 이름을 다중 단어로 변경
    props: {
      type: {
        type: String,
        default: 'primary',  // 기본 버튼 타입은 'primary'
      },
      disabled: {
        type: Boolean,
        default: false, // 버튼이 비활성화된 상태
      },
    },
    methods: {
      handleClick() {
        // 버튼 클릭 시 이벤트 처리
        if (!this.disabled) {
          this.$emit('click');
        }
      },
    },
  };
  </script>
  
  <style scoped>
  /* 기본 스타일 */
  .btn {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    transition: background-color 0.3s;
  }
  
  .btn-primary {
    background-color: #007bff;
    color: white;
  }
  
  .btn-primary:hover {
    background-color: #0056b3;
  }
  
  .btn-secondary {
    background-color: #6c757d;
    color: white;
  }
  
  .btn-secondary:hover {
    background-color: #5a6268;
  }
  
  .btn-disabled {
    background-color: #d6d6d6;
    cursor: not-allowed;
  }
  </style>
  