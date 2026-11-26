<script setup lang="ts">
const router = useRouter();

const items = [
  {
    label: 'Home',
    command: () => router.push('/')
  },
  {
    label: 'Cats',
    command: () => router.push('/cats')
  },
  {
    label: 'Kittens',
    command: () => router.push('/kittens')
  },
  {
    label: 'Nuustik',
    command: () => router.push('/kittens/nuustik')
  },
  {
    label: 'Murka',
    command: () => router.push('/kittens/murka')
  }
];
</script>

<template>
  <ClientOnly>
    <Menubar :model="items">
      <template #start>
        <strong>Blog</strong>
      </template>
    </Menubar>

    <NuxtPage />
  </ClientOnly>
</template>