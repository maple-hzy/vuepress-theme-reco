<template>
  <div class="post-item-container">
    <div class="title">
      <RouterLink :to="data.path">{{ data.title }}</RouterLink>
    </div>
    <PageInfo :page-data="data" :hide-views="false"> </PageInfo>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import PageInfo from './PageInfo.vue'

export default defineComponent({
  components: { PageInfo },

  props: {
    data: {
      type: Object,
      default: () => ({}),
    },
  },

  setup() {
    return {}
  },
})
</script>
