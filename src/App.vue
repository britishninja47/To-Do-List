<script setup>
import { ref, onMounted, computed, watch } from 'vue'

const name = ref('')
const todos = ref([])
const input_content = ref('')
const input_category = ref(null)

const input_basic = ref('')

const todos_asc = computed(() => todos.value.sort((a, b) => {
  return b.createdAt - a.createdAt
}))
</script>


<template>
<main class="app">
  <section class="greeting">
    <h2 class="title">
      Hey, how are you? <input type="text" placeholder="Name here" v-model="name" />
    </h2>
    <section>
      <h1 class="title">
        Todos: {{todos.length}}
      </h1>
    </section>
  </section>
</main>
</template>
