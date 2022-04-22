<template>
    <div class="flex justify-center">
        <div class="xl:h-screen xl:w-5/6 xl:rounded-3xl bg-dark-pink flex flex-col justify-start items-center">
            <div class="text-light-brown items-center flex flex-col lg:flex-row  xl:mt-4">
                <img src="@/assets/images/profile.jpg" alt="Profile image" class="h-80 w-80 m-4 xl:h-96 xl:w-96 xl:m-10 rounded-full">
                <div class="flex flex-col m-4 xl:m-10">
                    <h1 class="text-7xl xl:text-xxl font-black flex-wrap">Shivam Gupta</h1>
                    <p class="text-xl xl:text-2xl xl:mt-10">An efficient learner with a creative approach to problem solving
                        and experienced in the latest technologies of web development
                    </p>
                </div>
            </div>
            <div class="grid grid-cols-2 gap-0 w-full bg-light-brown justify-center items-center">

                <Head title="About"/>
                <PropList :property="personal">
                    <template v-slot:propName>
                        <PropName>Email:</PropName>
                        <PropName>Github:</PropName>
                    </template>
                    <template v-slot:propValue>
                        <PropLink :linkTo="emailVal">shivamrg36@gmail.com</PropLink>
                        <PropLink :linkTo="githubVal">Shivam755</PropLink>
                    </template>
                </PropList>

                <Head title="Education"/>
                <PropList :property="education"></PropList> 
                
                <Head title="Projects"/>
                <PropList>
                    <template v-slot:propValue>
                        <div v-for="pro in projects" class="my-5" :key="pro.name">
                            <PropLink :linkTo="pro.link" class="font-bold text-2xl xl:text-4xl">
                                {{pro.name}}
                            </PropLink>
                            <PropValue>
                                {{pro.description}}
                            </PropValue>
                        </div>
                    </template>
                </PropList>
            </div>
        
            <div class="xl:h-20 w-full xl:rounded-b-3xl bg-dark-pink"><br><br><br><br></div>
        </div>
    </div>
</template>

<script lang="ts">
import Head from '@/components/sectionHead.vue'
import PropName from '@/components/propName.vue'
import PropValue from '@/components/propValue.vue'
import PropLink from '@/components/propLink.vue'
import PropList from '@/components/propList.vue'

export default {
  name: 'IndexPage',
  data(){
      return{
          personal:{
              names:["Full Name", "Gender", "DOB", "Phone"],
              values:["Shivam Ramjiyawan Gupta", "Male", "10-JUL-2002", "+91 7045165072"]
          },
          emailVal:"mailto:shivamrg36@gmail.com",
          githubVal:"https://github.com/Shivam755",
          education:{
              names:["SSC", "HSC", "Graduation"],
              values:["S.S.S.S ENGLISH HIGH SCHOOL IN 2018", "S.K. SOMAIYA VINAYMANDIR IN 2020", "RAMNARAIN RUIA AUTONOMOUS COLLEGE IN 2023(EXPECTED)"]
          },
          projects:[
              {
                  name:"SOLAR METERING",
                  link:"https://github.com/Shivam755/SolarMetering",
                  description:"Web application using <b>Blockchain</b> and <b>ReactJS</b>"
              },
              {
                  name:"AUCTIONS",
                  link:"https://github.com/Shivam755/Auctions",
                  description:"A web application using <b>DJANGO, HTML, CSS</b> and <b>JavaScript</b>"
              },
              {
                  name:"HUBVERT",
                  link:"https://github.com/Shivam755/HubVert",
                  description:"A web application using <b>VueJS, API</b> and <b>local-storage</b>"
              },
              {
                  name:"INSTAGLONE",
                  link:"https://github.com/QuronXZ/Instaglone",
                  description:"An Instagram clone, created using <b>Flutter</b> and <b>Firebase</b>"
              },
              
          ],
      }
  },
  components:{
      Head,
      PropName,
      PropValue,
      PropLink,
      PropList
  },
  props:{
      title:{
          type:String,
          default:"Section Heading"
      },
  },
}
</script>