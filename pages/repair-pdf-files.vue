<template>
  <div>
    <SpecializedUtilityTemplate 
        :posts="featuresPosts"
    />
  </div>
</template>

<script>
import SpecializedUtilityTemplate from '~/components/SpecializedUtilities/SpecializedUtilityTemplate.vue';
import { getPosts } from '../ghost-api/posts.js'
import Vue from 'vue'

export default Vue.extend({
    name: "PDFChecker",
    components: { SpecializedUtilityTemplate },
    async asyncData() {
        const featuresPosts = await getPosts('hash-checker-feat')
        return {
            featuresPosts: featuresPosts.slice().reverse()
        }
    }
})
</script>
