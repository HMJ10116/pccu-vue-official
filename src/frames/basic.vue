<template>
  <div>
    <myNavigation class="fixed-top" :title="'履歷型教材'" :routes="routes"></myNavigation>
    <router-view class="marginForNavigation"/>
    <myFooter></myFooter>
  </div>
</template>
<script>
import myNavigation from "@/components/myNavigation.vue"
import myFooter from "@/components/myFooter.vue"
export default {
  data: () => ({
    routes: [
      {
        name: 'resume',
        text: '範本'
      },
      {
        name: 'overview',
        text: '入門'
      },
      {
        name: 'html',
        text: 'HTML'
      },
      {
        name: 'css',
        text: 'CSS'
      },
      {
        name: 'myWork',
        text: 'myWork'
      }
    ]
  }),
  components: {
    myNavigation,
    myFooter
  }
}
</script>
<style lang="scss">
.marginForNavigation {
  margin-top: 55px;
}
</style>
