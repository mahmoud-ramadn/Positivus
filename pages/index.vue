<template  lang="pug">
  div(class='container mx-auto md:px-24 px-2  ')
    div( class='grid md:grid-cols-2  grid-cols-1 justify-between ')
      div(class='col-span-1     flex justify-between flex-col  ') 
        h1(class='  text-7xl  font-medium  ') Navigating the digital landscape for success
        p(class='  text-xl font-normal    leading-8 ') Our digital marketing agency helps businesses grow and succeed online through a range of services including SEO, PPC, social media marketing, and content creation.
        button(class='  w-[264px] h-16 px-5   py-9 bg-black  text-white rounded-xl flex justify-center items-center ') Book a consultation
      div(class=' col-span-1') 
        img( src='/Images/hero.svg')

        //-  brand comapany
     
    div(class='  flex   justify-between   items-center mt-16 mb-36 flex-wrap ')
      img( src='/Images/brands/Company logo.svg')
      img( src='/Images/brands/Company logo (1).svg')
      img( src='/Images/brands/Company logo (2).svg')
      img( src='/Images/brands/Company logo (3).svg')
      img( src='/Images/brands/Company logo (4).svg')
      img( src='/Images/brands/Company logo (5).svg')

    //-  services section

    section(class='mb-20 ')
      div( class=' flex items-center   gap-[40px]   ')
        h3( class='  text-4xl  font-medium bg-primary  p-2 w-[178px]  rounded  text-center ') Services
        p( class=' md:w-[580px]   md:text-lg  text-sm ') At our digital marketing agency, we offer a range of services to help businesses grow and succeed online. These services include:

        //-  cards section

    section(class=' grid  md:grid-cols-2  grid-cols-1 gap-10 ')
      div(  v-for="(item, index) in CardsData " :key="index"    
            :class="{ 'bg-third' :item.title === 'Search engine' , 'bg-primary' : item.title ==='Pay-per-click',  'bg-black' :item.title==='Social Media' }" class='  border-black border-[1px] p-12       col-span-1   h-[310px]  rounded-[45px]  flex items-center justify-between')
        div( class=' flex justify-between  flex-col items-start md:w-[221px] h-[210px]')
          div
            h3( class='  text-3xl  font-medium   bg-primary  p-2  w-fit  rounded  text-center ' :class="{ 'bg-white' :  item.subtitle==='advertising' }") {{ item.title}}
            h3( class='  text-3xl  my-1 font-medium bg-primary  p-2  w-fit  rounded  text-center ' :class="{ 'bg-white' :  item.subtitle==='advertising' }") {{item.subtitle}}
          div( class=' flex items-center')
              button(class='w-[41px] h-[41px] rounded-full flex items-center  justify-center  bg-black') 
                Icon(name="mingcute:arrow-right-up-line" class=' text-[#B9FF66] font-medium ' width="24" height="24")
              span( class='  text-xl ') Learn more
        img(:src='item.img')
    section( class='  my-32 md:h-[357px]  bg-third  rounded-[45px]  px-14 flex justify-between items-center ')
      div( class='md:w-[500px] md:h-[277px]  space-y-7 ')
        h3(class=' text-3xl font-medium') Let’s make things happen
        p(class='  text-lg font-thin') Contact us today to learn more about how our digital marketing services can help your business grow and succeed online.
        button(class=' md:w-[288px] h-[68px] rounded-xl text-white bg-black flex items-center justify-center   text-xl ') Get your free proposal
      img( class=' h-full md:w-[360px]' src='/Images/Frame 19.svg')

    section(class='mb-20 ')
      div( class=' flex items-center   gap-[40px]   ')
        h3( class='  text-4xl  font-medium bg-primary  p-2  w-fit  rounded  text-center ') Case Studies
        p( class=' md:w-[580px]   md:text-lg  text-sm ') Explore Real-Life Examples of Our Proven Digital Marketing Success through Our Case Studies
    
    section( class='md:h-[326px] text-white  rounded-[45px] bg-black w-full  md:p-[70px] flex  justify-between items-center')
      div(class='md:w-[286px]  h-[115px]  space-y-5 ')
        p(class='  text-lg ') For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales.
        button( class=' flex items-center gap-3 text-primary ') learn more
          Icon(name="mingcute:arrow-right-up-line" class=' text-[#B9FF66] font-medium ' width="24" height="24")

      div( class=' md:w-[414px] h-[186px] border-x-2 border-white  flex justify-center items-center ')
        div(class='md:w-[286px]   h-[115px]  space-y-5  ')
          p(class='  text-lg ') For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales.
          button( class=' flex items-center gap-3 text-primary ') learn more
            Icon(name="mingcute:arrow-right-up-line" class=' text-[#B9FF66] font-medium ' width="24" height="24")

     
      div(class='md:w-[286px]  h-[115px]  space-y-5 ')
        p(class='  text-lg ') For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales.
        button( class=' flex items-center gap-3 text-primary ') learn more
          Icon(name="mingcute:arrow-right-up-line" class=' text-[#B9FF66] font-medium ' width="24" height="24")

    section(class='my-20 ')
      div( class=' flex items-center   gap-[40px]   ')
        h3( class='  text-4xl  font-medium bg-primary  p-2  w-fit  rounded  text-center ') Our Working Process 
        p( class=' md:w-[292px]    font-normal  md:text-lg  text-sm ') Step-by-Step Guide to Achieving Your Business Goals
    
    //-  toggeled rows

    section
      div(class=' w-full  bg-primary  text-black md:px-[60px] md:py-[41px] rounded-[45px] border-[1px] border-black   transition-all  duration-100   ease-linear overflow-hidden ' :class="toggledIcons ? 'h-[159px]' : 'h-[279px]'" )
        div(class=' flex justify-between  items-center')
          h2(class=' text-6xl font-medium flex  items-center  gap-x-5' ) 01 
            span(class=' text-3xl ') Consultation
          button( @click="handleToggledIcon"  type="button" class='  w-[58px] h-[58px] rounded-full flex items-center justify-center   bg-third border-[1px] border-black')
              Icon( :name="!toggledIcons ? 'typcn:minus' : 'uil:plus'" class=' text-4xl') 
        hr( v-if="!toggledIcons" class=' h-[2px] w-full  my-8 bg-black')
        
        p(v-if="!toggledIcons") During the initial consultation, we will discuss your business goals and objectives, target audience, and current marketing efforts. This will allow us to understand your needs and tailor our services to best fit your requirements.
        
    
    

    
</template>

<script setup lang="ts">
const toggledIcons=ref(false)

const handleToggledIcon=()=>{
  toggledIcons.value=!toggledIcons.value
}

const CardsData=[

{
  title:'Search engine',
  subtitle:'optimization',
  img:'/Images/cards/one.svg'
},
{
  title:'Pay-per-click',
  subtitle:'advertising',
  img:'/Images/cards/two.svg'
},
{
  title:'Social Media',
  subtitle:'Marketing',
  img:'/Images/cards/three.svg'
},
{
  title:'Email',
  subtitle:'Marketing',
  img:'/Images/cards/four.svg'
},
{
  title:'Content',
  subtitle:'Creation',
  img:'/Images/cards/five.svg'
},
{
  title:'Analytics and ',
  subtitle:'Tracking',
  img:'/Images/cards/six.svg'
},

]

</script>

<style scoped>

</style>