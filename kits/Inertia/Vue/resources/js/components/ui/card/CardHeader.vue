<script setup lang="ts">
import type { HTMLAttributes } from "vue"
import { cn } from "@/lib/utils"

const props = defineProps<{
  class?: HTMLAttributes["class"]
}>()
</script>

<template>
  <div
    data-slot="card-header"
    :class="cn('flex flex-col gap-1.5 px-6 has-data-[slot=card-action]:grid has-data-[slot=card-action]:auto-rows-min has-data-[slot=card-action]:grid-rows-[auto_auto] has-data-[slot=card-action]:items-start has-data-[slot=card-action]:grid-cols-[1fr_auto]', props.class)"
  >
    <slot />
  </div>
</template>
