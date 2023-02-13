<template>
  <div>
    <svg
      :src="post.feature_image"
      :class="svg_css"
    >
        <image :xlink:href="post.feature_image" :class="img_css"/>    
    </svg>
    <TitleBody 
      :title="post.title"
      :body="post.html"
      :title_css="title_css"
      :body_css="body_css"
      :hide_body="hide_body"
      :hide_title="hide_title"
    />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import TitleBody from './TitleBody.vue';

export default Vue.extend({
  name: 'TitleBodyImage',
  components: { TitleBody },
  props: {
    tag: {
      type: String,
      required: false,
    },
    title: {
      type: String,
      required: false,
    },
    body: {
      type: String,
      required: false,
    },
    title_css: {
      type: String,
      required: false,
    },
    body_css: {
      type: String,
      required: false,
    },
    img_css: {
      type: String,
      required: false,
    },
    hide_title: {
      type: Boolean,
      required: false,
    },
    hide_body: {
      type: Boolean,
      required: false,
    },
    post: {
        type: Object,
        required: false
    },
    svg_css: {
        type: String,
        required: false
    }
  }
})
</script>
