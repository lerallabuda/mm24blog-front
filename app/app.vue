<script setup lang="ts">
const route = useRoute();
</script>

<template>
  <ClientOnly>
    <ElMenu
      mode="horizontal"
      :default-active="route.path"
      :ellipsis="false"
      router
    >
      <ElMenuItem index="/">Home</ElMenuItem>
      <ElMenuItem index="/cats">Cats</ElMenuItem>
      <ElMenuItem index="/kittens">Kittens</ElMenuItem>
      <ElMenuItem index="/kittens/nuustik">Nuustik</ElMenuItem>
      <ElMenuItem index="/kittens/murka">Murka</ElMenuItem>
    </ElMenu>

    <NuxtPage />
  </ClientOnly>
</template>