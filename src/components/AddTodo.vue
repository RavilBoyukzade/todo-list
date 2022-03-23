<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="title" />
    <button class="submit">Create</button>
  </form>
</template>

    <script>
export default {
  data() {
    return {
      title: "",
    };
  },
  methods: {
    onSubmit() {
      if (this.title.trim()) {
        const newTodo = {
          id: Date.now(),
          title: this.title,
          completed: false,
        };
        this.$emit("add-todo", newTodo);
      }
    },
  },
};
</script>

<style scoped>
input {
  width: 350px;
  border-radius: 10px;
  border: 1px solid;
}
.submit {
  color: #1be41b;
  background-color: transparent;
  background-image: none;
  border-color: #1be41b;
  display: inline-block;
  font-weight: 350;
  text-align: center;
  white-space: nowrap;
  vertical-align: middle;
  user-select: none;
  border: 1px solid;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: 100px;
  margin-left: 10px;
}
.submit:hover {
  background-color: #1be41b;
  color: #fff;
}
</style>