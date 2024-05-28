<template>
  <div class="child-container">
    <h2>Child Component</h2>
    <button @click="updateMessage">Ganti Pesan</button>
    <button @click="emitData">Emit Data</button>
  </div>
</template>

<script>
export default {
  name: 'ChildComponent',
  methods: {
    updateMessage() {
      this.$emit('message-change', 'Hello from Fatur');
    },
    emitData() {
      const data = 'Some data from Fatur';
      this.$emit('data-emitted', data);
    }
  }
};
</script>

<style scoped>
.child-container {
  background-color: #e6f7ff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
}

h2 {
  color: #333;
}

button {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 10px 2px;
  cursor: pointer;
  border-radius: 4px;
}

button:hover {
  background-color: #e41010;
}
</style>
