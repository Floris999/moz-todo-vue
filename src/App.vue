<template>
  <!--Here is a javascript that says getElementById?-->
  <div id="app">
    <h1>To-Do List</h1>
    <to-do-form @todo-added="addToDo"></to-do-form>
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
import ToDoForm from "./components/ToDoForm.vue";
export default {
  //default export
  name: "App",
  components: {
    //component object
    ToDoItem, //register component
    ToDoForm
  },
  data() {
    return {
      ToDoItems: [
        { 
          label: "Learn to code", 
          done: false 
        },
        {
          
          label: "Set up basic Vue project",
          done: true,
        },
        {
          
          label: "Understand this data prop topic",
          done: false,
        },
        {
          
          label: "Show Erik-Jan that i master Vue.js",
          done: false,
        },
      ],
    };
  },
  methods: {
    addToDo(toDoLabel) {
      console.log("To-do added: ", toDoLabel); //task here is to add console.log of input that is added in label ,toDoLabel
    }
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

li {
  margin: 20px 5px;
}
</style>
