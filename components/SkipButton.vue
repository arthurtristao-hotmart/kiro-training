<script setup lang="ts">
import { useNav } from '@slidev/client'

const props = defineProps<{ to: number, label?: string }>()
const { go } = useNav()
</script>

<template>
  <button
    @click="go(props.to)"
    class="kiro-chip mt-4 hover:opacity-80 transition cursor-pointer border-none"
  >
    {{ label ?? `Ir para slide ${props.to}` }}
  </button>
</template>