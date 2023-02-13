<template>
  <div class="w-screen min-h-screen flex flex-col items-center">
    <h1></h1>

    <ToolFeatures :posts="posts" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ToolFeatures from './ToolFeatures.vue'

export default Vue.extend({
  components: { ToolFeatures },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
})
</script>
