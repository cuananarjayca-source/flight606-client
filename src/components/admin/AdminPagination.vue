<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  currentPage: { type: Number, required: true },
  totalPages: { type: Number, required: true },
  pageNumbers: { type: Array, required: true },
});

const emit = defineEmits(['go-to-page', 'first-page', 'last-page', 'prev-page', 'next-page']);

const firstPage = () => emit('go-to-page', 1);
const lastPage = () => emit('go-to-page', props.totalPages);
const prevPage = () => emit('go-to-page', Math.max(1, props.currentPage - 1));
const nextPage = () => emit('go-to-page', Math.min(props.totalPages, props.currentPage + 1));
</script>

<template>
  <div class="admin-pagination" v-if="totalPages > 1">
    <button
      class="pagination-btn"
      :disabled="currentPage === 1"
      @click="firstPage"
    >
      First
    </button>
    <button
      class="pagination-btn"
      :disabled="currentPage === 1"
      @click="prevPage"
    >
      Prev
    </button>

    <button
      v-for="page in pageNumbers"
      :key="page"
      v-if="page === 'left-ellipsis' || page === 'right-ellipsis'"
      class="pagination-ellipsis"
      disabled
    >
      …
    </button>

    <button
      v-for="page in pageNumbers"
      :key="page"
      v-if="typeof page === 'number'"
      class="pagination-btn"
      :class="{ active: page === currentPage }"
      @click="$emit('go-to-page', page)"
    >
      {{ page }}
    </button>

    <button
      class="pagination-btn"
      :disabled="currentPage === totalPages"
      @click="nextPage"
    >
      Next
    </button>
    <button
      class="pagination-btn"
      :disabled="currentPage === totalPages"
      @click="lastPage"
    >
      Last
    </button>
  </div>
</template>


