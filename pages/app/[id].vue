<script setup lang="js">
useHead({
  title: 'My App',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  bodyAttrs: {
    class: 'test'
  }
})
const getdata = ( x )=>{
  console.log(x)
}
const data2 = ref(1)
const appId = useRoute().params.id
console.log(appId)

const {data: res} = await useFetch('https://hub.grapps.cn/app-server/marketui/859a51f9bb3b48b5bfd222e3bef56425/apps/' + appId + '/detail')

</script>

<template>
  <div v-html="res.desc">
  </div>
</template>

<style scoped>

</style>