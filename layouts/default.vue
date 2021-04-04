<template>
  <div>
    <Header/>
    <div class="main">
      <Sidebar/>
      <Nuxt />
    </div>
  </div>
</template>
<script>
import Header from "@/components/header";
import Sidebar from "@/components/sidebar";
export default {
  components: {Sidebar,Header}
}
</script>
<style>
.main {
  @apply
  h-full
  flex flex-row
}
</style>
