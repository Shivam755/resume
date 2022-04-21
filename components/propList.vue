<template>
  <div class="m-4 xl:m-10 flex flex-row text-xl xl:text-3xl text-dark-gray">
    <ul class="xl:ml-10">
      <div v-if="property!=={}">
        <PropName v-for="name in property.names" :key="name">
          {{name}}:
        </PropName>
      </div>
      <slot name="propName">

      </slot>
    </ul>
    <ul class="ml-4 xl:ml-10">
      <div v-if="property!=={}">
        <PropValue v-for="value in property.values" :key="value">
          {{value}}
        </PropValue>
      </div>
      <slot name="propValue">

      </slot>
    </ul>
  </div>
</template>

<script lang="ts">
import PropName from '@/components/propName.vue'
import PropValue from '@/components/propValue.vue'


export default {
  name: 'PropList',
  components:{
    PropName,
    PropValue
  },
  props:{
      property:{
          type:Object,
          default:{}
      },
  },
}
</script>