<template> <!--Here is a javascript that says getElementById?-->
  <div id="app">
    <h1>To-Do List</h1>
    <ul>
      <li>
        <to-do-item label="My ToDo Item" :done="true"></to-do-item>
      </li> <!--rendering component-->
    </ul>
  </div>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue";
export default { //default export
  name: 'App',
  components: { //component opbject
    ToDoItem //register component
  }
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
