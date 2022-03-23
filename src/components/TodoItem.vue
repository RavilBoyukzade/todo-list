<template>
  <div>
    <li>
       <span v-bind:class="{ done: todo.completed }">
     <!-- <input type="checkbox" v-on:change="todo.completed = !todo.completed" /> -->
     <input type="checkbox" />
        <strong>{{ todo.id }}</strong>
        {{ todo.title }}
      </span>
      <button class="btn-delete" v-on:click="$emit('remove-todo', todo.id)">&times;</button>
    </li>
  </div>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true
    },
  },
};
</script>

<style scoped>
li {
  border: 1px solid black;
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
  padding: 10px 20px;
}
.btn-delete {
  color: #dc3545;
  background-color: transparent;
  background-image: none;
  border-color: #dc3545;
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
}
.btn-delete:hover {
  background-color: #dc3545;
  color: #fff;
}
input {
  margin-right: 10px;
}

.done {
  text-decoration: line-through;
}
</style>