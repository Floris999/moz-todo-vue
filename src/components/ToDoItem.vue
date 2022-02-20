<template>
    <div>
        <input type="checkbox" :id="id" :checked="isDone"/>
        <label :for="id">{{label}}</label><!--label prop input-->
    </div>

</template>
<script>
import uniqueId from 'lodash.uniqueid';
    export default {
        props: {
            label: {
                required: true,
                type: String
            },
            done: {
                default: false,
                type: Boolean
            },
            id: {
                required: true,
                type: String
            }
        },
        data() {
            return {
                isDone: this.done, // returning results of prop done/or every prop? (not sure yet)
                num: uniqueId("todo-") //changed ID to num because of duplicate error
            };
        }
    };
</script>