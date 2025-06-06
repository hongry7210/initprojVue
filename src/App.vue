<template>
  <v-app>
    <v-main>
      <BaseButton type="primary" @click="handlePrimaryClick">Primary Button</BaseButton>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import BaseButton from './components/Button.vue';

export default {
  name: 'App',
  components: {
    BaseButton,
  },
  methods: {
    handlePrimaryClick() {
      alert('Primary Button Clicked');
    },
    handleSecondaryClick() {
      alert('Secondary Button Clicked');
    },
  },
  data: () => ({
    //
  }),
}
</script>
