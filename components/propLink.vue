<template>
    <li>
        <a class="no-underline hover:underline" :href="linkTo" target="_blank">
            <slot>
        
            </slot>
        </a>
    </li>
</template>

<script lang="ts">

export default {
  name: 'PropLink',
  props:{
      linkTo:{
          type:String,
          default:"#"
      }
  }
}
</script>