<script setup lang="ts">
import Card from "../components/card.vue"
const objet = {nom:"maison", prix:"43", image:"../../public/pexels_binyamin_mellish_106399_1.jpg", nbrSDB:"2"}
</script>
<template>
    <div class="p-2">
        <h1 class="text-2xl">Page Simple</h1>
    <Card nom="test" :prix="30" image="../../public/pexels_binyamin_mellish_106399_1.jpg" nbrSDB="3" favori="true"/>
    <Card v-bind="objet"/>
    </div>
</template>
