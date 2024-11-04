<template>
  <select v-model="$i18n.locale">
    <option v-for="locale in $i18n.availableLocales" :key="`locale-${locale}`" :value="locale">{{ locale }}</option>
      {{ locale }}
  </select>
  <h1> {{ $t("messages.hello",{name,surname})}} </h1>
  <p> {{ $t("messages.content",{description}) }} </p>
  <p> {{ $t("messages.products",{count:1})}}</p>
  <p> {{ $t("messages.comments",5) }}</p>
</template>
  
<script lang="ts" setup>
  import {ref} from 'vue';
  const name = ref('Manuel');
  const description = ref('Description');
  const surname = ref('Garcia');
</script>
  
<style scoped>
</style>
  