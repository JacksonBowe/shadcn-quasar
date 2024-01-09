<script setup lang="ts">
import { DropdownMenuItem, type DropdownMenuItemProps } from 'radix-vue'
import { cn } from '@/lib/utils'

const props = defineProps<DropdownMenuItemProps & { inset?: boolean; class?: string }>()
</script>

<template>
  <DropdownMenuItem
    v-bind="props"
    :class="[
    	cn(
    		'tw-relative tw-flex tw-cursor-default tw-select-none tw-items-center tw-rounded-sm tw-px-2 tw-py-1.5 tw-text-sm tw-outline-none tw-transition-colors focus:tw-bg-accent focus:tw-text-accent-foreground data-[disabled]:tw-pointer-events-none data-[disabled]:tw-opacity-50',
    		inset && 'pl-8',
    		props.class,
    	),
    ]"
  >
    <slot />
  </DropdownMenuItem>
</template>
