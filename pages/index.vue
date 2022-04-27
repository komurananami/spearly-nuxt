<template>
  <spearly-content-list id="news">
    <template v-slot="item">
      <nuxt-link :to="`/${item.content.attributes.publicUid}`">
        {{ item.content.values.title }}
        <img :src="item.content.values.image" />
        {{ item.content.values.description }}
        {{ item.content.values.date }}
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
