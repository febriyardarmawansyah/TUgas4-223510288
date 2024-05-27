<template>
  <div class="nested-component">
    <p>Komponen Nested C</p>
  </div>
</template>

<script>
export default {
  name: 'NestedComponentC',
};
</script>

<style scoped>
.nested-component {
  padding: 20px;
  background: linear-gradient(135deg, #1b8bb4, #ff99cc); /* Gradient warna merah ke pink muda */
  border-radius: 12px;
  text-align: center;
  margin-top: 20px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4); /* Bayangan yang lebih menonjol */
  transition: transform 0.3s, box-shadow 0.3s; /* Animasi transisi */
}

/* Optional hover effect */
.nested-component:hover {
  transform: translateY(-3px); /* Efek naik sedikit pada hover */
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.6); /* Bayangan yang lebih menonjol saat hover */
}
</style>
