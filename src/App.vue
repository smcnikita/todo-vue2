<template>
  <div id="app">
    <div class="main">
      <header-items/>
      <task-field/>
      <list-item/>
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
  }
}
</script>

<style>
@import "./assets/css/style.min.css";
</style>
