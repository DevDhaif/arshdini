<template>
    <form @submit.prevent="add">
            <div class="flex justify-between space-x-4">
                <input v-model="newTodo" type="text" class="w-full p-2 border border-gray-500 rounded text-black">
                <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded">Add</button>
            </div>
        </form>
</template>
<script>
export default{
    data(){
        return{
            newTodo: '',
        }
    },
    methods:{
        add(e){
            this.$emit('add', this.newTodo)
            
        }
    }
}
</script>