<template>
  <div class="main__list">
    <div class="main__list-item">
      <div class="main__list-item-check">
        <check-icon/>
      </div>
      <p>выполнить что-то</p>
      <div class="main__list-item-remove">
        <remove-icon/>
      </div>
    </div>

    <div class="main__list-item main__list-item--completed">
      <div class="main__list-item-check">
        <check-icon/>
      </div>
      <p>выполнено</p>
      <div class="main__list-item-remove">
        <remove-icon/>
      </div>
    </div>
  </div>
</template>

<script>
import RemoveIcon from "@/components/icons/RemoveIcon";
import CheckIcon from "@/components/icons/CheckIcon";

export default {
  name: "ListItem",
  components: {
    RemoveIcon,
    CheckIcon
  }
}
</script>

<style scoped>

</style>