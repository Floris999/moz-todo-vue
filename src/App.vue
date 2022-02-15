<template>
  <!--Here is a javascript that says getElementById?-->
  <div id="app">
    <h1>To-Do List</h1>
    <ul>
      <li v-for="item in ToDoItems" :key="item.id">
        <to-do-item :label="item.label" :done="item.done" :id="item.id"></to-do-item>
      </li>
      <!--rendering component-->
    </ul>
  </div>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue";
export default {
  //default export
  name: "App",
  components: {
    //component object
    ToDoItem, //register component
  },
  data() {
    return {
      ToDoItems: [
        { id: uniqueId("todo-"), label: "Lean to code", done: false },
        {
          id: uniqueId("todo-"),
          label: "Set up basic Vue project",
          done: true,
        },
        {
          id: uniqueId("todo-"),
          label: "Understand this data prop topic",
          done: false,
        },
        {
          id: uniqueId("todo-"),
          label: "Show Erik-Jan that i master Vue.js",
          done: false,
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

ul {
  list-style-type: none;
}
</style>
