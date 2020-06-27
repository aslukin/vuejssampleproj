<template>
    <div>
        <ul>
            <TodoItem />
            
            
            <li>todo 1</li>
            <li>todo 2</li>
            <li>todo 3</li>
        </ul>
    </div>
</template>

<script>
import TodoItem from '@/components/TodoItem'
export default {
    components: {
        TodoItem
    }
    
}
</script>