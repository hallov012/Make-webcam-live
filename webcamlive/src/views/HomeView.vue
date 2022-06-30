<template>
  <div class="home">
    <MainPage />
  </div>
</template>

<script>
// @ is an alias to /src
import MainPage from '@/components/MainPage/MainPage.vue'

export default {
  name: 'HomeView',
  components: {
    MainPage
  }
}
</script>

