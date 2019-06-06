<template lang="pug">
  section
    div.cards
      book-detail-item
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import BookDetailItem from '~/components/BookDetailItem.vue';

@Component({
  components: {
    BookDetailItem
  }
})
export default class BookDetail extends Vue {}
</script>
<style lang="sass">

.cards
  display: flex
  flex-wrap: wrap
  justify-content: flex-between

.row
  padding: 8px 0
</style>