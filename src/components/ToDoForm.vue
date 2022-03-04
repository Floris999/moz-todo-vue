<template>
    <form v-on:submit.prevent="onSubmit">
        <label for="new-todo-input">What needs to be done?</label>
        <input class="input__lg" type="text" id="new-todo-input" name="new-todo" autocomplete="off" v-model.trim.lazy="label"/>
        <button class="btn btn__primary btn__lg" type="submit">Add</button>
    </form>
</template>

<script>
  export default {
    methods: {
        onSubmit() {
            if(this.label === "") {
            return;
            } 
            this.$emit("todo-added", this.label);
            this.label = "";
        }
    },
    data() {
        return {
            label: ""
        };
    } 
  };
</script>

