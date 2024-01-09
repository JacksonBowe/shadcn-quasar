<script setup lang="ts">
import { DropdownMenuLabel, type DropdownMenuLabelProps } from 'radix-vue'
import { cn } from '@/lib/utils'

const props = defineProps<DropdownMenuLabelProps & {
	inset?: boolean
	class?: string
}>()
</script>

<template>
  <DropdownMenuLabel
    v-bind="props"
    :class="cn('tw-px-2 tw-py-1.5 tw-text-sm tw-font-semibold',
    	inset && 'tw-pl-8', props.class)"
  >
    <slot />
  </DropdownMenuLabel>
</template>
