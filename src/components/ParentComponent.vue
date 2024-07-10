<template>
  <div class="parent-container">
    <h1>Parent Component</h1>
    <p>Data from GrandChild: {{ dataFromGrandChild }}</p>
    <ChildComponent @data-from-grandchild="handleDataFromGrandChild">
      <template v-slot:slotName>
        <p>This is a slot content inside ChildComponent</p>
      </template>
    </ChildComponent>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  components: {
    ChildComponent
  },
  data() {
    return {
      dataFromGrandChild: ''
    };
  },
  methods: {
    handleDataFromGrandChild(data) {
      this.dataFromGrandChild = data;
    }
  }
};
</script>

<style scoped>
.parent-container {
  border: 2px solid #42b983;
  padding: 20px;
  margin: 20px;
  border-radius: 10px;
  background-color: #f9f9f9;
}

h1 {
  color: #42b983;
}

p {
  font-size: 16px;
}
</style>
