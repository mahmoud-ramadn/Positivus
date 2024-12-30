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
      div( v-for="(item, index) in ToggeledDroblist" :key="index" class=' w-full my-3   text-black md:px-[60px] md:py-[41px] rounded-[45px] border-[1px]   border-b-8  border-black   transition-all  duration-100   ease-linear overflow-hidden ' 
          :class="[!item.isToggled ? 'h-[159px]' : 'h-[279px]', !item.isToggled ? 'bg-primary' : 'bg-third']")
        div(class=' flex justify-between  items-center')
          h2(class=' text-6xl font-medium flex  items-center  gap-x-5' ) {{item.num}}
            span(class=' text-3xl ') {{item.titel}}
          button( @click="handleToggledIcon(index)"  type="button" class='  w-[58px] h-[58px] rounded-full flex items-center justify-center   bg-third border-[1px] border-black')
              Icon( :name="item.isToggled  ? 'typcn:minus' : 'uil:plus'" class=' text-4xl') 
        hr( v-if="item.isToggled" class=' h-[2px] w-full  my-8 bg-black')
        
        p(v-if="item.isToggled") {{item.des}}
    
    section(class=' my-36 ')
      div( class=' flex items-center   gap-[40px]   ')
        h3( class='  text-4xl  font-medium bg-primary  p-2  w-fit  rounded  text-center ') Team
        p( class=' md:w-[468px]    font-normal  md:text-lg  text-sm ') Meet the skilled and experienced team behind our successful digital marketing strategies
          
    section
      div(class='  grid md:grid-cols-3     grid-cols-1  gap-10  items-center   ')
        div( v-for="(member, index) in TeamData" :key="index" class=' col-span-1  h-[331px] md:px-6 md:py-9  rounded-[45px] border-[1px]   border-b-4  border-black  flex-col justify-center items-center flex  ') 
          div(class='md:w-[317px]  md:h-[227px] flex flex-col items-center justify-between ' )
            div(class=' flex justify-between  gap-2 border-b-[1px] border-black pb-5 ')
              img(:src="member.avarat" alt="altText")
              div( class=' self-end')
                h4 {{member.titel}}
                p(class=' w-28') {{member.jobTitle}}
              button(class=' w-[41px] h-[41px] rounded-full flex items-center justify-center bg-black ')
                Icon(name="grommet-icons:linkedin-option" width="24" height="24"  class=' text-primary')
            p(class='  text-lg  font-thin ') {{member.des}}  
      div(class=' w-full flex justify-end  my-10')
        button(class=' md:w-[268px]  h-[68px]  rounded-xl text-white bg-black  flex  items-center justify-center ')  See all team     
    
    section(class=' my-36 ')
      div( class=' flex items-center   gap-[40px]   ')
        h3( class='  text-4xl  font-medium bg-primary  p-2  w-fit  rounded  text-center ') Testimonials
        p( class=' md:w-[468px]    font-normal  md:text-lg  text-sm ') Hear from Our Satisfied Clients: Read Our Testimonials to Learn More about Our Digital Marketing Services
    //- tesimaials

    div(class=' w-full md:h-[625px]  rounded-[45px] bg-black pt-[84px] pb-[68px]')
      div(class='   overflow-x-scroll  flex items-center gap-x-12 justify-center ')
        div(class='  space-y-14')
          div(class='md:w-[606px] h-[237px] rounded-[45px]  border-[1px] border-primary p-12 text-white relative ')
            p "We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."
            div(class="w-0 h-0 border-t-[1px] border-b-[1px] border-l-[1px] border-r[20px] border-transparent border-r-primary")
          div(class='     pl-12 ')
            h4(class=' text-lg  text-primary font-thin') John Smith
            p(class=' text-white') Marketing Director at XYZ Corp
        div(class='  space-y-14')
          div(class='md:w-[606px] h-[237px] rounded-[45px]  border-[1px] border-primary p-12 text-white relative ')
            p "We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."
            div(class="w-0 h-0 border-t-[1px] border-b-[1px] border-l-[1px] border-r[20px] border-transparent border-r-primary")
          div(class='     pl-12 ')
            h4(class=' text-lg  text-primary font-thin') John Smith
            p(class=' text-white') Marketing Director at XYZ Corp
        div(class='  space-y-14')
          div(class='md:w-[606px] h-[237px] rounded-[45px]  border-[1px] border-primary p-12 text-white relative ')
            p "We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."
            div(class="w-0 h-0 border-t-[1px] border-b-[1px] border-l-[1px] border-r[20px] border-transparent border-r-primary")
          div(class='     pl-12 ')
            h4(class=' text-lg  text-primary font-thin') John Smith
            p(class=' text-white') Marketing Director at XYZ Corp
        div(class='  space-y-14')
          div(class='md:w-[606px] h-[237px] rounded-[45px]  border-[1px] border-primary p-12 text-white relative ')
            p "We have been working with Positivus for the past year and have seen a significant increase in website traffic and leads as a result of their efforts. The team is professional, responsive, and truly cares about the success of our business. We highly recommend Positivus to any company looking to grow their online presence."
            div(class="w-0 h-0 border-t-[1px] border-b-[1px] border-l-[1px] border-r[20px] border-transparent border-r-primary")
          div(class='     pl-12 ')
            h4(class=' text-lg  text-primary font-thin') John Smith
            p(class=' text-white') Marketing Director at XYZ Corp
      //- indcators
      div(class=' w-full    mt-14   flex justify-center  items-center  gap-x-8 ')
        button 
          Icon(name="cuida:arrow-left-outline"  class=' text-white text-xl ')
        div(class=' flex  gap-4 items-center')
          img(src='/Images/star.svg' alt='img')
          img(src='/Images/whiteStart.svg' alt='img')
          img(src='/Images/whiteStart.svg' alt='img')
          img(src='/Images/whiteStart.svg' alt='img')
          img(src='/Images/whiteStart.svg' alt='img')
          img(src='/Images/whiteStart.svg' alt='img')
        button   
          Icon(name="cuida:arrow-right-outline"  class=' text-xl text-white')
        //-  contacts us

    section(class=' my-36 ')
      div( class=' flex items-center   gap-[40px]   ')
        h3( class='  text-4xl  font-medium bg-primary  p-2  w-fit  rounded  text-center ') Contact Us
        p( class=' md:w-[468px]    font-normal  md:text-lg  text-sm ') Connect with Us: Let's Discuss Your Digital Marketing Needs
      
      div(class='  w-full md:h-[773px]  rounded-[45px] my-20  py-20 bg-third  overflow-hidden pl-[100px]  pt-[60xp] pb-[80px] flex  relative  justify-between   items-center ')
        div(class='md:w-[556px] md:h-[633px]     space-y-10 ')
          div(class=' flex  items-center gap-x-3')
            input(type="radio" id="hi")
            label( for='hi' class=' text-black  text-lg font-medium') Say Hi
            input(type="radio" id="get")
            label( for='get' class=' text-black  text-lg font-medium') Get a Quote
          form
            label( for='name' class='  text-base    font-medium text-black') Name
            input(class='md:w-[559px]  h-[59px] mt-[4px] mb-[24px] border-[1px]  border-black  outline-[1px]  focus:outline-black rounded-xl pl-6 '  type='text' id='name' placeholder='Name')
            
            label( for='email' class='  text-base  font-medium  text-black') Email*
            input(class='md:w-[559px]  h-[59px] mt-[4px] mb-[24px]  border-[1px]  border-black  outline-[1px]  focus:outline-black rounded-xl pl-6 '  type='email' id='email' placeholder='email')
            
            label( for='name' class='  text-base    font-medium text-black') Message*
            textarea(class='md:w-[559px] mt-[4px] mb-[24px] border-[1px]  border-black  outline-[1px]  focus:outline-black rounded-xl  p-3 '  id='Message' placeholder='Message')
            button(class='md:w-[556px]  h-[68px]   rounded-xl  bg-black text-white text-xl  focus:outline-black  font-medium ') Send Message
        img( class='hidden md:block md:w-[691px] md:h-[648px]   absolute  top-1/2   -translate-y-1/2   -right-60  z-20 ' src='/Images/form.svg')

</template>

<script setup lang="ts">

const handleToggledIcon = (index) => {
      ToggeledDroblist.value[index].isToggled = !ToggeledDroblist.value[index].isToggled;
    };


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


const ToggeledDroblist = ref([
  {
    num: '01',
    titel: 'Consultation',
    des: 'During the initial consultation, we will discuss your business goals...',
    isToggled: false
  },
  {
    num: '02',
    titel: 'Research and Strategy Development',
    des: 'During the initial consultation, we will discuss your business goals...',
    isToggled: false
  },
  {
    num: '03',
    titel: 'Implementation',
    des: 'During the initial consultation, we will discuss your business goals...',
    isToggled: false
  },
  {
    num: '04',
    titel: 'Monitoring and Optimization',
    des: 'During the initial consultation, we will discuss your business goals...',
    isToggled: false
  },
  {
    num: '05',
    titel: 'Reporting and Communication',
    des: 'During the initial consultation, we will discuss your business goals...',
    isToggled: false
  },
  {
    num: '06',
    titel: 'Continual Improvement',
    des: 'During the initial consultation, we will discuss your business goals...',
    isToggled: false
  }
]);

// Team data

const TeamData=ref([

{
  avarat:'/Images/Picture.svg',
  title:'Mahmoud',
  jobTitle:'CEO and Founder',
  des:' 10+ years of experience in digital marketing. Expertise in SEO, PPC, and content strategy    '
},
{
  avarat:'/Images/Picture.svg',
  title:'Emily Johnson',
  jobTitle:'PPC Manager',
  des:' 3+ years of experience in paid search advertising. Skilled in campaign management and performance analysis   '
},
{
  avarat:'/Images/Picture.svg',
  title:'Brian Williams',
  jobTitle:'Social Media Specialist',
  des:' 2+ years of experience in writing and editing Skilled in creating compelling, SEO-optimized content for various industries'
},
{
  avarat:'/Images/Picture.svg',
  title:'Michael Brown',
  jobTitle:'Senior SEO Specialist',
  des:' 5+ years of experience in SEO and content creation. Proficient in keyword research and on-page optimization  '
},
{
  avarat:'/Images/Picture.svg',
  title:'Jane Doe',
  jobTitle:'Director of Operations',
  des:' 7+ years of experience in project management and team leadership. Strong organizational and communication skills   '
},
{
  avarat:'/Images/Picture.svg',
  title:'Ramadn mahmoud',
  jobTitle:'CEO and Founder',
  des:' 10+ years of experience in digital marketing. Expertise in SEO, PPC, and content strategy    '
},


])
  



</script>

<style scoped>



</style>