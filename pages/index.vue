<template>
    <div class="flex justify-center">
        <div class="h-screen w-5/6 rounded-3xl bg-dark-pink flex flex-col justify-start items-center">
        <div class="text-light-brown flex flex-row  mt-4">
            <img src="@/assets/images/profile.jpg" alt="Profile image" class="h-96 w-96 m-10 rounded-full">
            <div class="flex flex-col m-10">
                <h1 class=" text-xxl font-black flex-wrap">Shivam Gupta</h1>
                <p class="text-2xl mt-10">An efficient learner with a creative approach to problem solving
                    and experienced in the latest technologies of web development
                </p>
            </div>
        </div>
        <div class="grid grid-cols-2 gap-0 w-full bg-light-brown justify-center items-center">
            <Head title="About"/>
            <div class="mx-10 my-10 flex flex-row text-3xl text-dark-gray">
                <ul  class="ml-10">
                    <li><b>Full Name:</b></li>
                    <li><b>Gender:</b></li>
                    <li><b>DOB:</b></li>
                    <li><b>Phone:</b></li>
                    <li><b>Email:</b></li>
                    <li><b>Github:</b></li>
                </ul>
                <ul  class="ml-10" >
                    <li> Shivam Ramjiyawan Gupta</li>
                    <li>Male</li>
                    <li>10-JUL-2002</li>
                    <li>+91 7045165072</li>
                    <li><a class="no-underline hover:underline" href="mailto:shivamrg36@gmail.com" target="_blank">shivamrg36@gmail.com</a></li>
                    <li><a class="no-underline hover:underline" href="https://github.com/Shivam755" target="_blank">Shivam755</a></li>
                </ul>
            </div>

            <Head title="Education"/>
            <div class="flex flex-row ml-10 my-10 pr-10 text-3xl text-dark-gray">
                <ul  class="ml-10">
                    <li><b>SSC:</b></li>
                    <li><b>HSC:</b></li>
                    <li><b>Graduation:</b></li>
                </ul>
                <ul  class="ml-10" >
                    <li>
                        <p>
                            S.S.S.S ENGLISH HIGH SCHOOL IN 2018
                        </p>
                    </li>
                    <li>
                        <p>
                            S.K. SOMAIYA VINAYMANDIR IN 2020
                        </p>
                    </li>
                    <li>
                        <p>
                            RAMNARAIN RUIA AUTONOMOUS COLLEGE IN 2023(EXPECTED)
                        </p>
                    </li>
                </ul>
            </div> 
            
            <Head title="Projects"/>
            <div class="flex flex-row ml-10 my-10 text-3xl text-dark-gray">
                <ul class="ml-10">
                    <li class="my-5">
                        <h1><a class="no-underline hover:underline font-bold text-4xl" href="https://github.com/Shivam755/SolarMetering" target="_blank">SOLAR METERING</a></h1>
                        <p>
                            Web application using <b>Blockchain</b> and <b>ReactJS</b>
                        </p>
                    </li>
                    <li class="my-5">
                        <h1><a class="no-underline hover:underline font-bold text-4xl" href="https://github.com/Shivam755/Auctions" target="_blank">AUCTIONS</a></h1>
                        <p>
                            A web application using <b>DJANGO, HTML, CSS</b> and <b>JavaScript</b>
                        </p>
                    </li>
                    <li class="my-5">
                        <h1><a class="no-underline hover:underline font-bold text-4xl" href="https://github.com/Shivam755/HubVert" target="_blank">HUBVERT</a></h1>
                        <p>
                            A web application using <b>VueJS, API</b> and <b>local-storage</b>
                        </p>
                    </li>
                    <li class="my-5">
                        <h1><a class="no-underline hover:underline font-bold text-4xl" href="https://github.com/QuronXZ/Instaglone" target="_blank">INSTAGLONE</a></h1>
                        <p>
                            An Instagram clone, created using <b>Flutter</b> and <b>Firebase</b>
                        </p>
                    </li>
                </ul>
            </div> 
        </div>
        
        <div class="h-20 w-full rounded-b-3xl bg-dark-pink"><br><br><br><br></div>
    </div>
    </div>
</template>

<script lang="ts">
import Head from '@/components/sectionHead.vue'

export default {
  name: 'IndexPage',
  components:{
      Head
  },
  props:{
      title:{
          type:String,
          default:"Section Heading"
      },
  },
}
</script>