<template>
  <button :class="[props.type]">{{ props.text }}</button>
</template>
<script setup lang="ts">
interface Props {
  text: string;
  type: "primary" | "secondary" | "tertiary";
}

const props = withDefaults(defineProps<Props>(), {
  text: "Vu Nguyen",
});

console.log(props.text);
console.log(props.type);
</script>
