<template>
  <button type="button" @click="showBlock = !showBlock">
    Toggle block
  </button>
  <Block v-if="showBlock" />
</template>

<script setup>
import { ref } from 'vue';
import Block from './Block.vue';

const showBlock = ref(false);
</script>
