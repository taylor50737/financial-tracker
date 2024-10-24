<template>
  <UModal v-model="isOpen">
    <UCard :uri="{ divide: 'divide-y divide-gray-100 dark:divide-gray-800' }">
      <template #header>Add Transaction </template>
      <div>Hello!</div>
    </UCard>
  </UModal>
</template>

<script setup>
const props = defineProps({
  modelValue: Boolean,
});
const emit = defineEmits(["update:modelValue"]);

const isOpen = computed({
  get: () => props.modelValue,
  set: (value) => emit("update:modelValue", value),
});
</script>
