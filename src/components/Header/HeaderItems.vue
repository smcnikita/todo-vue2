<template>
  <div class="main__header">
    <div class="main__header-list">
      <list-icon/>
    </div>
    <h2>To do</h2>
    <div class="main__header-add">
      <plus-icon/>
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
  }
}
</script>

<style scoped>

</style>