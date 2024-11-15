<template> 
    <section class="space-y-8">
        <todo-list :todos="filters.inProgressTodos" title="In Progress"></todo-list>
        <todo-list :todos="filters.completedTodos" title="Completed"></todo-list>
        <create-todo @add="add"
        ></create-todo>
    </section>
</template>
<script>
import todoList from './TodoList.vue'
import CreateTodo from './CreateTodo.vue'
export default {
    components: { 'todo-list': todoList , 'create-todo': CreateTodo},
    data() {
        return {
            todos: [
                { id: 1, name: 'Learn Vue', inProgress: true },
                { id: 2, name: 'Learn React', inProgress: true },
                { id: 3, name: 'Learn Angular', inProgress: false },
                { id: 4, name: 'Learn Laravel', inProgress: false },
                { id: 5, name: 'Learn Django', inProgress: false },
            ],
            
        }
    },
    methods:{
        add(newTodo){
            console.log(newTodo)
            if (!newTodo.trim()) return;
            this.todos.push({
                id: this.todos.length + 1,
                name: newTodo,
                inProgress: false
            })
            newTodo = ''
        }
    },
    computed: {
        filters (){
            return {
                inProgressTodos: this.todos.filter(todo => !todo.inProgress),
                completedTodos: this.todos.filter(todo => todo.inProgress)
            }
        }
    }
}
</script>