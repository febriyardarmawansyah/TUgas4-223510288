<template>
  <div class="parent-component">
    <h2 style="color: #333;">Komponen Utama</h2>
    <p style="font-style: italic; color: #666;">Data yang Diterima: {{ receivedData }}</p>
    <ChildComponentA @data-from-a="handleDataFromA"/>
    <ChildComponentB @data-from-b="handleDataFromB"/>
    <NestedComponentC />
    <div class="slot-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import ChildComponentA from './ChildComponentA.vue';
import ChildComponentB from './ChildComponentB.vue';
import NestedComponentC from './NestedComponentC.vue';

export default {
  name: 'ParentComponent',
  components: {
    ChildComponentA,
    ChildComponentB,
    NestedComponentC
  },
  data() {
    return {
      receivedData: ''
    };
  },
  methods: {
    handleDataFromA(data) {
      this.receivedData = data;
    },
    handleDataFromB(data) {
      this.receivedData = data;
    }
  }
};
</script>

<style scoped>
.parent-component {
  border: 2px solid #ddd;
  border-radius: 10px;
  background-color: #f5f5f5; /* Warna abu-abu lebih muda */
  padding: 20px;
  text-align: center;
  margin-top: 20px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Bayangan yang lebih menonjol */
}

.slot-content {
  padding: 10px;
  background-color: #f0f8ff; /* Warna biru muda */
  border-radius: 8px;
  margin-top: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Bayangan yang lebih lembut */
}
</style>
