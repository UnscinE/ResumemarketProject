<script setup lang="ts">
</script>

<template>

  <div>
    <header>
      <nav class="navbar">
        <RouterLink to="/">หน้าแรก (Home)</RouterLink> |
        <RouterLink to="/about">เกี่ยวกับเรา (About)</RouterLink>
      </nav>
    </header>

    <main class="content">
      <RouterView />
    </main>

  </div>
</template>

<style>
@import "tailwindcss";
</style>
