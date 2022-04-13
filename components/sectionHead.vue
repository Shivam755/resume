<template>
    <h1 class="ml-10 mt-10 text-8xl text-right text-dark-pink">{{title}}</h1>
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