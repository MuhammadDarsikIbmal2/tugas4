<template>
  <div class="child-container">
    <h2>Child Component</h2>
    <slot name="slotName"></slot>
    <GrandChildComponent @send-data="emitDataToParent"></GrandChildComponent>
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue';

export default {
  components: {
    GrandChildComponent
  },
  methods: {
    emitDataToParent(data) {
      this.$emit('data-from-grandchild', data);
    }
  }
};
</script>

<style scoped>
.child-container {
  border: 2px solid #35495e;
  padding: 15px;
  margin: 20px;
  border-radius: 10px;
  background-color: #e3f2fd;
}

h2 {
  color: #35495e;
}
</style>
