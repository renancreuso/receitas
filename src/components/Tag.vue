<template>
  <span :class="['tag',{ativa}]">
    {{ texto }}
  </span>
</template>

<script lang="ts">
export default {
  props: {
    texto: { type: String, requerid: true },
    ativa: Boolean
  },
};
</script>

<style>
.tag {
  display: inline-block;
  border-radius: 0.5rem;
  min-width: 4.25rem;
  padding: 0.5rem;
  text-align: center;
  transition: 0.2s;
  color: var(--cinza);
  background: var(--cinza-claro);
  font-size: 400;
}
.tag.ativa {
  color: var(--creme, #fffaf3);
  background: var(--coral, #f0633c);
  font-weight: 700;
}
</style>
