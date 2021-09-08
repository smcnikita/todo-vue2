<template>
  <div class="main__add-field">
    <input type="text" placeholder="добавить новую задачу..."/>
    <button class="main__add-field-btn">
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
  }
}
</script>

<style scoped>

</style>