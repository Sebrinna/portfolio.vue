<template>
  <nav class="bg-success-subtle">
    <h1>Vue Router 링크 방식들</h1>
    <a href="http://naver.com">naver</a><br>
    <a href="/">1-Home</a> &nbsp;
    <RouterLink to="/">2-Home</RouterLink><br>
    <a href="/about">1-About me</a> &nbsp;
    <RouterLink to="/about">2-About me</RouterLink><br>

    <button @click="$router.push('/')">3-Home</button>
    <button @click="goAbout">3-About me</button>

    <router-link to="/about">4-About me</router-link>
    <!-- 옛날 방식 -->

  </nav>

</template>

<script setup>
import { useRouter } from 'vue-router';

  const router = useRouter();

  const goAbout = ()=>{
    router.push('/about')
  }
</script>

<style lang="scss" scoped></style>