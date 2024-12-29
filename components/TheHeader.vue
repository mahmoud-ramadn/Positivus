<template  lang="pug" >
  div(class=' container mx-auto my-16 px-24   flex justify-between items-center')
    NuxtLink(  to="/" class=' flex items-center   gap-3 ')
      img( src='/Images/logo.svg' alt="altText")
      h1(class='  font-medium text-3xl ')  POSTIVUS
    ul( class='  md:flex items-center gap-10 text-xl text-black  hidden ')
      li  
        NuxtLink( to="about" class=' hover:bg-primary  p-2  rounded-md' ) About us
      li  
        NuxtLink( to="about" ) Services
      li  
        NuxtLink( to="about" ) Use Cases
      li  
        NuxtLink( to="about" ) Pricing
      li  
        NuxtLink( to="about" ) Blog
      li
        button(class='  rounded-xl  h-16  w-56  border-[1px] border-black hover:bg-primary hover:text-white ')  Request a quote
   
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>