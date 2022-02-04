<template>
    <div>
        <input type="checkbox" id="todo-item" :checked="IsDone"/>
        <label for="todo-item">{{label}}</label><!--label prop input-->
    </div>

</template>
<script>
    export default {
        props: {
            label: {
                required: true,
                type: String
            },
            done: {
                default: false,
                type: Boolean
            }
        },
        data() {
            return {
                isDone: this.done // returning results of prop done/or every prop? (not sure yet)
            };
        }
    };
</script>