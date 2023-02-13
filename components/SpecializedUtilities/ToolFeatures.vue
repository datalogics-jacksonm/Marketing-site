<template>
  <div class="grid grid-cols-3 max-w-screen-lg gap-8">
      <TitleBodyImage 
        v-for="(post, index) in posts" 
        :key="index" 
        :post="post"
        :svg_css="'w-12 h-12 bg-primary fill-white rounded-xl p-3'"
        :img_css="'w-8 h-8 fill-white'"
        :title_css="'text-xl font-white text-filson'"
        :body_css="'text-base font-primary text-venn'"
        class="flex flex-col items-center text-center space-y-4"
      />
  </div>
</template>

<script>
import Vue from 'vue';
import TitleBodyImage from '../TitleBodyImage.vue';

export default Vue.extend({
  components: { TitleBodyImage },
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
})
</script>
