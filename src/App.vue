<template>
  <div id="app">
    <div class="main">
      <header-items/>
      <task-field @onAddTask="onAddTask"/>

      <div class="main__list">
        <template v-if="listTasks.length === 0">
          <h2>Задач нет :)</h2>
        </template>
        <template v-else>
          <list-item
              v-for="(task, index) in listTasks"
              :key="index"
              :text="task.text"
              :checked="task.checked"
              :indexTask="index"
              @onToggleCompleted="onToggleCompleted(index)"
              @removeTasks="removeTasks(index)"
          />
        </template>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderItems from "@/components/Header/HeaderItems";
import TaskField from "@/components/TaskField";
import ListItem from "@/components/ListItem";

export default {
  name: 'App',
  components: {
    HeaderItems,
    TaskField,
    ListItem
  },
  data() {
    return {
      listTasks: []
    }
  },
  methods: {
    onToggleCompleted(indexTask) {
      this.listTasks[indexTask].checked = !this.listTasks[indexTask].checked;
    },
    removeTasks(indexTask) {
      this.listTasks.splice(indexTask, 1);
    },
    onAddTask(text) {
      this.listTasks.push({
        text: text,
        checked: false
      });
    }
  }
}
</script>

<style>
@import "./assets/css/style.min.css";

.main {
  padding-bottom: 70px;
}

h2 {
  color: #cecece;
  text-align: center;
  margin-top: 50px;
}
</style>
