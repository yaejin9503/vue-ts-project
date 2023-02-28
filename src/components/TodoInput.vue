<!-- eslint-disable prettier/prettier -->
<template>
  <div>
    <label for="todo-input">오늘 할 일 : </label>
    <input id="todo-input" type="text" :value="item" @input="handleInput" />
    <button @click="addTodo" type="button">add</button>
  </div>
</template>
<!-- eslint-disable prettier/prettier -->
<script lang="ts">
/* eslint-disable prettier/prettier */
import Vue from "vue";
export default Vue.extend({
  props: ["item"],
  methods: {
    handleInput(event: any) {
      this.$emit("input", event.target.value);
    },
    addTodo() {
      this.$emit("add");
    },
  },
});
</script>
<style scoped></style>
