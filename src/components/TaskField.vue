<template>
  <div class="main__add-field">
    <input id="new-task" @keyup.13="addTask()" type="text" placeholder="добавить новую задачу..." v-model="text"/>
    <button class="main__add-field-btn" @click="addTask()">
      <plus-icon/>
    </button>
  </div>
</template>

<script>
import PlusIcon from "@/components/icons/PlusIcon";

export default {
  name: "TaskField",
  components: {
    PlusIcon
  },
  data() {
    return {
      text: ""
    }
  },
  methods: {
    addTask() {
      if (this.text.length > 0) {
        this.$emit('onAddTask', this.text)
        this.text = "";
        document.getElementById('new-task').focus();
      }
    }
  }
}
</script>

<style scoped>
input {
	caret-color: var(--black);
	color: var(--black);
}
</style>
