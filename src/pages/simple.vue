<script setup lang="ts">
import Card from "../components/card.vue"
const objet = {nom:"maison", prix:"43", nbrSDB:"2"}
</script>
<template>
    <Card nom="test" :prix="30" nbrSDB="3" favori="true"/>
    <Card v-bind="objet"/>
</template>
