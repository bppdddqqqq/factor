<template>
  <h3 class="entry-subtitle">{{ post.synopsis }}</h3>
</template>
<script lang="ts">
import { stored } from "@factor/api"

export default {
  props: {
    postId: { type: String, default: "" },
  },
  computed: {
    post(this: any) {
      return stored(this.postId) || {}
    },
  },
}
</script>
<style lang="less" scoped>
.entry-subtitle {
  color: var(--color-text-secondary);
  font-size: 1.2em;
  line-height: 1.6em;
  margin: 0.5em 0em;
}
</style>
