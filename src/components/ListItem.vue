<template>
  <div
      class="main__list-item"
      :class="{'main__list-item--completed': checked}">
    <div class="main__list-item-check" @click="toggleCompleted(indexTask)">
      <check-icon/>
    </div>
    <p>
      <template v-if="checked">
        <s>{{ text }}</s>
      </template>
      <template v-else>
        {{ text }}
      </template>
    </p>
    <div class="main__list-item-remove" @click="removeTasks(indexTask)">
      <remove-icon/>
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
  },
  props: {
    'text': String,
    'checked': Boolean,
    'indexTask': Number
  },
  methods: {
    toggleCompleted(indexTask) {
      this.$emit('onToggleCompleted', indexTask)
    },
    removeTasks(indexTask) {
      this.$emit('removeTasks', indexTask)
    }
  }
}
</script>

<style scoped>

</style>