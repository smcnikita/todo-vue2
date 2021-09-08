<template>
  <div class="main__header">
    <div class="main__header-list">
      <list-icon id="list-icon"/>
    </div>
    <h2>{{ listTitle }}</h2>
    <div class="main__header-add">
      <plus-icon id="plus-icon"/>
    </div>
  </div>
</template>

<script>
import PlusIcon from "@/components/icons/PlusIcon";
import ListIcon from "@/components/icons/ListIcon";

export default {
  name: "HeaderItems",
  components: {
    PlusIcon,
    ListIcon
  },
  data() {
    return {
      listTitle: "To do"
    }
  }
}
</script>

<style scoped>
#list-icon,
#plus-icon {
  display: none;
}
</style>