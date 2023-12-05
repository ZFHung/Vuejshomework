<script setup>
import { defineProps, computed } from "vue"

const props = defineProps({
  books: {
    type: Array,
    required: true,
    default: [],
  },
})

const bookCount = computed(() => {
  return props.books.filter((book) => book.title.length > 2).length
})
</script>

<template>
  <h2 class="text-2xl" v-if="books.length == 0">Not Anything</h2>
  <h2 class="text-2xl" v-else>目前共有 {{ bookCount }} 個事項</h2>
</template>
