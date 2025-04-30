<template>
  <div>Block with internal reactive data</div>
</template>

<script setup>
import { onBeforeMount, ref } from 'vue';

const data = ref({});

onBeforeMount(loadData);

async function loadData() {
  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/photos');

    data.value = await response.json();

    console.log(11111, data.value);
  } catch (e) {
    console.log(e);
  }
}
</script>
