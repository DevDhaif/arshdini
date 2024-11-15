<template>
    <section v-show="todos.length" class="mt-8">
        <h2 class="font-bold mb-2">this is title {{ title }}:</h2>
        <ul class="border border-gray-500 divide-y divide-gray-500">
            <todo v-for="todo in todos" :key="todo.id" :todo="todo"></todo>
        </ul>
    </section>
</template>
<script>
import Todo from './Todo.vue'
export default {
    components: { 'todo': Todo },
    props: {
        todos: {
            type: Array,
        },
        title: {
            type: String,
            required: true
        }
    }
}
</script>