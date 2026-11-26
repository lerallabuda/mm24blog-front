<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui';

const items: NavigationMenuItem[] = [
  {
    label: 'Home',
    to: '/'
  },
  {
    label: 'Cats',
    to: '/cats'
  },
  {
    label: 'Kittens',
    to: '/kittens'
  },
  {
    label: 'Nuustik',
    to: '/kittens/nuustik'
  },
  {
    label: 'Murka',
    to: '/kittens/murka'
  }
];
</script>

<template>
  <ClientOnly>
    <UApp>
      <UHeader title="Blog">
        <UNavigationMenu :items="items" />

        <template #right>
          <UColorModeButton />
        </template>
      </UHeader>

      <NuxtRouteAnnouncer />

      <UContainer>
        <NuxtPage />
      </UContainer>
    </UApp>
  </ClientOnly>
</template>