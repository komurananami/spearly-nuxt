<template>
  <spearly-content-list id="news">
    <template v-slot="item">
      <nuxt-link :to="`/news/${item.content.attributes.publicUid}`">
        {{ item.content.values.title }}
        <img :src="item.content.values.image" />
        {{ item.content.values.description }}
        {{ $dayjs(item.content.values.date).format(`YYYY-MM-DD`) }}
      </nuxt-link>
    </template>
  </spearly-content-list>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',
})
</script>
