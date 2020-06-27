<template>
    <li>
        <span v-bind:class="{done: todo.completed}">
            <input type="checkbox" v-on:change="todo.completed = !todo.completed">
            <strong>{{todo.id}}</strong>
            {{todo.title}}
        </span>
        <button class="clearbtn">&times;</button>
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

<style scoped>
    li{
        border: 1px solid;
        border-color: #863636;
        display: flex;
        justify-content: space-between;
        padding: .5rem 2rem;
        margin-bottom: 1rem;
    }
    input{
        margin-right: 1rem;
    }
    .clearbtn{
        background-color: red;
        font-weight: 700;
        border-radius: 50%;
        border: none;
    }
    .clearbtn:focus{
        border: none;
        outline: none;
    }
    .done{
        text-decoration: line-through;
    }
</style>

