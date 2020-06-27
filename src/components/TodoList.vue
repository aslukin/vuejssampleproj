/* eslint-disable vue/valid-v-for */
<template>
    <div>
        <ul>
            <TodoItem 
                v-for="todo in todos"
                :key="todo"
                v-bind:todo="todo"
            />
            
            
            <li>todo 1</li>
            <li>todo 2</li>
            <li>todo 3</li>
        </ul>
    </div>
</template>

<script>
import TodoItem from '@/components/TodoItem'
export default {
    props: ['todos'],
    components: {
        TodoItem
    }
    
}
</script>


<style scoped>
    ul {
        list-style: none;
        margin: 0;
        padding: 0;
    }
</style>