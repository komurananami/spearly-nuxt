<template>
  <spearly-content :id="current">
    <template v-slot="content">
      <header>
        <h1>{{ content.values.title }}</h1>
      </header>
      <div v-html="content.values.description" />
      <img :src="content.values.image" />
      {{ $dayjs(content.values.date).format(`YYYY-MM-DD`) }}
    </template>
  </spearly-content>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',

  computed: {
    current() {
      return this.$route.params.id
    },
  },
})
</script>
