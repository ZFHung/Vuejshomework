<script setup>
import { ref, defineEmits } from "vue"

const bookName = ref("")

const emits = defineEmits(["add-book"])

const addBook = () => {
  emits("add-book", bookName.value)
  bookName.value = ""
}
</script>

<template>
  <div class="flex items-center gap-2 mt-4">
    <input
      v-model.trim="bookName"
      @keydown.enter="addBook"
      type="text"
      class="input input-bordered input-primary w-full max-w-xs"
    />
    <button @click="addBook" class="btn btn-primary">Add Something</button>
  </div>
</template>
