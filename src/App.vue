<script setup>
import { ref } from 'vue'

const displayRecipe = ref(false)

const toggleDisplayRecipe = () => {
  displayRecipe.value = !displayRecipe.value
}
</script>

<template>
  <div>
    <h1>Les Recettes de Maëlis</h1>
    <nav class="border border-blue-500 flex gap-x-6">
      <a>Accueil</a>
      <a>Afficher recette</a>
    </nav>
    <button class="my-3 border border-red-400">Ajouter une recette</button>
    <div v-if="displayRecipe" class="border border-black flex flex-col gap-y-2">
      <h2>Moelleux au chocolat</h2>
      <p>Recette rapide et gourmande de mon moelleux au chocolat</p>
      <h3>Ingrédients</h3>
      <ul>
        <li>200g de chocolat</li>
        <li>125g de sucre</li>
      </ul>
    </div>
    <button @click="toggleDisplayRecipe" class="mt-3 border border-red-400">
      Afficher recette
    </button>
  </div>
</template>

<!-- <style scoped></style> -->
