<template>
    <h1 class="mr-10 xl:ml-10 mt-2 xl:mt-10 text-4xl xl:text-8xl text-right xl:text-right text-dark-pink">{{title}}</h1>
</template>

<script lang="ts">

export default {
  name: 'Head',
  props:{
      title:{
          type:String,
          default:"Section Heading"
      },
  },
}
</script>