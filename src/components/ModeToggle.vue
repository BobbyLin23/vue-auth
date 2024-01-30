<script setup lang="ts">
import { useDark, useToggle } from '@vueuse/core'
import { MoonIcon, SunIcon } from '@radix-icons/vue'
import { Button } from './ui/button'

const isDark = useDark()

const toggleDark = useToggle(isDark)
</script>

<template>
  <Button variant="outline" size="icon" @click="toggleDark()">
    <SunIcon v-if="isDark" class="h-5 w-5" />
    <MoonIcon v-else class="h-5 w-5" />
  </Button>
</template>
