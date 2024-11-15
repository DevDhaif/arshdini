<template>
    <li>
        <label class="flex justify-between p-2">
            <span> {{ todo.name }} </span>
            <input type="checkbox" v-model="todo.inProgress">
        </label>
    </li>
</template>

<script>
export default {
    props: {
        todo: {
            type: Object,
            required: true
        }
    }
}
</script>