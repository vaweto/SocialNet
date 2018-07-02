<template>
    <tr>
        <th>{{task.id}}</th>
        <th>{{task.title}}</th>
        <th>{{task.priority}}</th>
        <th><button @click="remove" class="btn btn-danger">Remove</button></th>
    </tr>
</template>

<script>
    export default{
        data() {
            return{

            }
        },

        methods: {
          remove() {
              this.$emit('delete', this.task.id)
          }
        },
        props: ['task']
    }
</script>

<style>

</style>