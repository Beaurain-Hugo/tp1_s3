<script setup lang="ts">
import Bath from "./icones/bath.vue";
import Heart from "./icones/heart.vue";

defineProps({
    nom: String,
    prix: Number,
    favori: Boolean,
    image: String, // les images sont simplement l'URL absolue (depuis la racine, débute par '/' )
    nbrSDB: Number,
  })
</script>

<template>
  <figure>
    <!-- Pour changer la valeur d'un attribut on utilise un "binding" :
    https://vuejs.org/guide/essentials/template-syntax.html#attribute-bindings 
    Ici on affecte à l'attribut 'src' la 'props' "image" -->
    <img class="w-full h-48 object-cover" src="../../public/pexels_binyamin_mellish_106399_1.jpg" alt="" />
    <figcaption
      class="relative flex flex-col border-2 border-t-0 border-indigo-100"
    >
      <!-- Pour changer une classe CSS en fonction d'un booléen : 
      https://vuejs.org/guide/essentials/class-and-style.html#binding-html-classes -->
      <heart :class="{ 'fill-red-300': favori }" />

      <!-- Pour afficher du contenu textuel, simplement utiliser l'interpolation par double accolades (qui contiendront le JS dont l'interpretation donne le résultat affiché). -->
      <div class="text-2xl font-bold text-indigo-500 pr-1">${{ prix }}</div>

      <h3 class="text-2xl text-gray-900">{{ nom }}</h3>

      <hr class="border-indigo-100 border-t-2 my-4" />

      <div><bath class="inline-block pr-1" />{{ nbrSDB }} Bathrooms</div>
    </figcaption>
  </figure>
</template>