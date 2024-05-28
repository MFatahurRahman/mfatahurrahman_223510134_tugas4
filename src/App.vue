<template>
  <div id="app">
    <ParentComponent />
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';
import './assets/styles.css';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
};
</script>
