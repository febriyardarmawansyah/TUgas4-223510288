<template>
  <div class="child-component">
    <button class="send-button" @click="sendDataToParent">Kirim Data dari B</button>
  </div>
</template>

<script>
export default {
  name: 'ChildComponentB',
  methods: {
    sendDataToParent() {
      this.$emit('data-from-b', 'Data dari Komponen B');
    }
  }
};
</script>

<style scoped>
.child-component {
  margin: 10px;
  padding: 20px;
  background-color: #0099cc; /* Warna biru */
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4); /* Bayangan yang lebih menonjol */
  transition: transform 0.3s, box-shadow 0.3s; /* Animasi transisi */
}

.send-button {
  padding: 12px 24px;
  background-color: #66ccff; /* Warna biru muda */
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: background-color 0.3s; /* Animasi transisi */
}

.send-button:hover {
  background-color: #0077b3; /* Warna biru lebih gelap saat hover */
}

.child-component:hover {
  transform: translateY(-3px); /* Efek naik sedikit pada hover */
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.6); /* Bayangan yang lebih menonjol saat hover */
}
</style>
