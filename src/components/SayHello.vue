<template>
  <div>
    <p class="fs-5 fst-italic">{{ name }} sagt: Hallo!</p>
    <button @click="emit('greeting', 'Hi!')" class="btn btn-primary mx-auto d-block">Greet Back</button>
  </div>
</template>
<script setup lang="ts">
interface Props {
  name: string;
}

interface Emits {
  (event: 'greeting', msg: string): void;
}

defineProps<Props>();
const emit = defineEmits<Emits>();
</script>
