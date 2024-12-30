<template  lang="pug">
  div(class=' container mx-auto  px-24 ')
    div(class=' md:h-[514px] rounded-tr-[45px] md:px-[60px] md:py-[50px] rounded-tl-[45px] bg-[#191A23] ')
      div(class=' flex  justify-between items-center ')
        div(class='flex items-center gap-4')
          img( class=' w-[29px] h-[29px]' src='/Images/whiteStart.svg' alt="altText")
          h2(class=' text-2xl   font-medium  text-white') Positivus
        ul(class='md:w-[501px] md:flex items-center  justify-between hidden ')
          li(class='  text-white  underline-offset-4 underline decoration-[1px] decoration-slate-200 ') About us
          li(class='  text-white underline-offset-4 underline decoration-[1px] decoration-slate-200 ') About us
          li(class='  text-white  underline-offset-4 underline decoration-[1px] decoration-slate-200 ') About us
          li(class='  text-white  underline-offset-4 underline decoration-[1px] decoration-slate-200 ') About us
          li(class='  text-white underline-offset-4 underline decoration-[1px] decoration-slate-200 ') About us
        div(class=' flex items-center  gap-3')
          Icon(name="entypo-social:linkedin-with-circle"  class=' bg-white text-3xl' )
          Icon(name="grommet-icons:facebook" w  class=' bg-white text-3xl' )
          Icon(name="formkit:twitter"    class=' text-3xl bg-white' )
      div(class='flex  items-start justify-between md:flex-row flex-col my-[60px]')
        div(class='md:w-[332px] h-[132px] space-y-5 text-white')
          button(class='   md:w-[126px] md:h-[26px] rounded-md text-black bg-primary text-xl  ') Contact us:
          p(class=' text-sm') Email: info@positivus.com
          p(class='text-sm') Phone: 555-567-8901
          p(class='text-sm') Address: 1234 Main St
          p(class='text-sm') Moonstone City, Stardust State 12345
        div(class='md:w-[634px] md:h-[184px] rounded-xl  bg-[#292A32] p-[40px] flex items-center justify-between gap-x-6')
          input( type="email"   placeholder=" Email"  class='md:w-[285px] bg-transparent border-[1px] border-black  placeholder:text-sm   outline-black   focus:outline-black h-[65px] rounded-lg  pl-5 ')
          button(  type='button'  class='md:w-[285px]  bg-primary text-black font-normal  text-sm h-[65px] rounded-lg  pl-5 ') Subscribe to news
      hr(class=' h-[1px] bg-white w-full  my-10')
      div(class=' flex  items-center gap-4 mt-5')
        p(class='text-sm  font-thin  text-white') © 2023 Positivus. All Rights Reserved. 
        p(class='text-sm font-thin text-white  underline-offset-4 underline decoration-[1px] decoration-slate-200 ') Privacy Policy
         
      



    
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>