<template>
  <div class="container">
    <header class="header">
      <h1>Page Mobile First</h1>
      <p>
        Cette page commence en version mobile puis devient responsive avec Vue +
        Vite.
      </p>
    </header>

    <main class="layout">
      <section class="card">
        <h2>Contenu principal</h2>
        <p>Version mobile : 1 colonne. Version desktop : 2 colonnes.</p>
        <button class="button" @click="action">Action principale</button>
      </section>

      <aside class="card">
        <h2>Barre latérale</h2>
        <p>Cette zone devient une sidebar en desktop.</p>
      </aside>
    </main>
  </div>
</template>

<script setup>
const action = () => {
  alert("Bouton cliqué 🚀");
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background: #f5f7fb;
  color: #1f2937;
}

h1 {
  color: black;
}

h2 {
  color: #1f2937;
}

.container {
  max-width: 1200px;
  margin: auto;
  padding: 16px;
}

.header {
  background: white;
  padding: 20px;
  border-radius: 12px;
  margin-bottom: 16px;
}

.layout {
  display: grid;
  gap: 16px;
}

.card {
  background: white;
  padding: 20px;
  border-radius: 12px;
}

.button {
  margin-top: 12px;
  padding: 10px;
  background: black;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

/* Responsive */
@media (min-width: 768px) {
  .layout {
    grid-template-columns: 2fr 1fr;
  }
}
</style>
