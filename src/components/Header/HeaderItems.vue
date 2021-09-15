<template>
  <div class="main__header">
    <div class="main__header-list">
      <list-icon id="list-icon"/>
    </div>
    <h2>{{ listTitle }}</h2>
    <div class="main__header-add">
      <plus-icon id="plus-icon"/>
    </div>
		<div class="main__header-theme" @click="toggleTheme()">
			<theme-icon/>
		</div>
  </div>
</template>

<script>
import PlusIcon from "@/components/icons/PlusIcon";
import ListIcon from "@/components/icons/ListIcon";
import ThemeIcon from "@/components/icons/ThemeIcon";

export default {
  name: "HeaderItems",
  components: {
    PlusIcon,
    ListIcon,
		ThemeIcon
  },
  data() {
    return {
      listTitle: "To do"
    }
  },
	methods: {
		toggleTheme() {
			let theme = localStorage.theme;
			if(theme === 'dark') {
				this.trans();
				document.documentElement.setAttribute('data-theme', 'light');
				localStorage.theme = 'light';
				theme = 'dark';
			} else {
				this.trans();
				document.documentElement.setAttribute('data-theme', 'dark');
				localStorage.theme = 'dark';
				theme = 'light';
			}
		},
		trans() {
				document.documentElement.classList.add('transition');
				window.setTimeout(() => {
					document.documentElement.classList.remove('transition')
				}, 1000);
		}
	}
}
</script>

<style scoped>

</style>
