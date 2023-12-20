<template>
  <div class="bg-white">
    <main>
      <TheHeader></TheHeader>
      <TheContent></TheContent>

      <div class="bg-red-500" id="about">hello</div>
      <TheFooter></TheFooter>
    </main>
  </div>
</template>

<script setup>
import TheHeader from './components/TheHeader.vue'
import TheContent from './components/TheContent.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<style scoped>
.dropdown-trigger::after {
  display: inline-block;
  margin-left: 0.255em;
  vertical-align: 0.255em;
  content: '';
  border-top: 0.3em solid;
  border-right: 0.3em solid transparent;
  border-bottom: 0;
  border-left: 0.3em solid transparent;
}

* {
  transition: all 1s;
}
</style>
