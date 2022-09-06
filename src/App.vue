<template>
  <div class="flex justify-center items-center min-h-screen">
    <div class="bg-white w-96 p-8 rounded-lg">
      <h1 class="text-3xl font-bold">ToDo</h1>
      <ul class="my-4 max-h-96 overflow-y-auto">
        <li v-for="(task, index) in tasks" :key="index">{{ task }}</li>
      </ul>
      <input class="w-full border border-black rounded-md p-1"
        type="text" placeholder="Add new task"
        v-model="newTask" @keyup.enter="addNewTask" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'ToDo',
  data() {
    return {
      newTask: null,
      tasks: [
        "Task number one",
        "Task number two",
        "Another task",
        "Yet another task"
      ]
    }
  },
  methods: {
    addNewTask() {
      if(this.newTask != null) {
        this.tasks.push(this.newTask);
        this.newTask = null;
      }
    }
  }
}
</script>

<style scoped>
</style>
