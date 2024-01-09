<script setup lang="ts">
import {
	DropdownMenuContent,
	type DropdownMenuContentEmits,
	type DropdownMenuContentProps,
	DropdownMenuPortal,
	useForwardPropsEmits,
} from 'radix-vue'
import { cn } from '@/lib/utils'

const props = withDefaults(
	defineProps<DropdownMenuContentProps & { class?: string }>(),
	{
		sideOffset: 4,
	},
)
const emits = defineEmits<DropdownMenuContentEmits>()

const forwarded = useForwardPropsEmits(props, emits)
</script>

<template>
  <DropdownMenuPortal>
    <DropdownMenuContent
      :class="[
      	cn(
      		'tw-z-50 tw-min-w-[8rem] tw-overflow-hidden tw-rounded-md tw-border tw-bg-popover tw-p-1 tw-text-popover-foreground tw-shadow-md data-[state=open]:tw-animate-in data-[state=closed]:tw-animate-out data-[state=closed]:tw-fade-out-0 data-[state=open]:tw-fade-in-0 data-[state=closed]:tw-zoom-out-95 data-[state=open]:tw-zoom-in-95 data-[side=bottom]:tw-slide-in-from-top-2 data-[side=left]:tw-slide-in-from-right-2 data-[side=right]:tw-slide-in-from-left-2 data-[side=top]:tw-slide-in-from-bottom-2',
      		props.class,
      	),
      ]"
      v-bind="forwarded"
    >
      <slot />
    </DropdownMenuContent>
  </DropdownMenuPortal>
</template>
