<template>
  <div class="grandchild-container">
    <h3>GrandChild Component</h3>
    <button @click="sendData">Send Data to Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendData() {
      this.$emit('send-data', 'Hello from GrandChildComponent!');
    }
  }
};
</script>

<style scoped>
.grandchild-container {
  border: 2px solid #ff6347;
  padding: 10px;
  margin: 20px;
  border-radius: 10px;
  background-color: #fff3e0;
}

h3 {
  color: #ff6347;
}

button {
  background-color: #ff6347;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #e5533d;
}
</style>
