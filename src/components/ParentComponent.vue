<template>
    <div>
      <h1>Parent Component</h1>
      <p>Pesan: {{ message }}</p>
      <ChildComponent @message-change="handleMessageChange" @data-emitted="displayData" />
      <p>Data from Rahman: {{ childData }}</p>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildComponent
    },
    data() {
      return {
        message: 'Hello from Rahman',
        childData: ''
      };
    },
    methods: {
      handleMessageChange(newMessage) {
        this.message = newMessage;
      },
      displayData(data) {
        this.childData = data;
      }
    }
  };
  </script>
  
  <style scoped>
 
.parent-container {
  background-color: #f0f8ff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
  margin-bottom: 20px;
}

h1 {
  color: #333;
}

p {
  color: #666;
}

  </style>
  