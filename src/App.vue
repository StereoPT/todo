<template>
  <div class="flex justify-center items-center min-h-screen">
    <div class="bg-white p-8 rounded-lg">
      <h1 class="text-3xl font-bold">ToDo</h1>
      <ul>
        <li v-for="(task, index) in tasks" :key="index">{{ task }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ToDo',
  data() {
    return {
      tasks: [
        "Task number one",
        "Task number two",
        "Another task",
        "Yet another task"
      ]
    }
  }
}
</script>

<style scoped>
</style>
