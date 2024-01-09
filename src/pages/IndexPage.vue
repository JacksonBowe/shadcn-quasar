<template>
  <q-page class="row items-center justify-evenly">
    <SButton>Click me</SButton>
	<SDropdownMenu>
    <SDropdownMenuTrigger>Dropdown</SDropdownMenuTrigger>
    <SDropdownMenuContent>
      <SDropdownMenuLabel>My Account</SDropdownMenuLabel>
      <SDropdownMenuSeparator />
      <SDropdownMenuItem>Profile</SDropdownMenuItem>
      <SDropdownMenuItem>Billing</SDropdownMenuItem>
      <SDropdownMenuItem>Team</SDropdownMenuItem>
      <SDropdownMenuItem>Subscription</SDropdownMenuItem>
    </SDropdownMenuContent>
  </SDropdownMenu>
  </q-page>
</template>

<script setup lang="ts">
import { SButton } from '@/components/ui/button'
import {
	SDropdownMenu,
	SDropdownMenuContent,
	SDropdownMenuItem,
	SDropdownMenuLabel,
	SDropdownMenuSeparator,
	SDropdownMenuTrigger,
} from '@/components/ui/dropdown-menu'
</script>
