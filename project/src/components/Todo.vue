<template>
    <div>
        <input type="checkbox" :checked="todo.checked"/>
        <span class="ml-3"> {{ todo.text }}</span>  
    </div>
</template>

<script>
    export default
    {
        name: 'TodoItem',
        props: {
            todo: {
                type: Object,
                required: true,
            }
        }
    };
</script>

<style scoped>
</style>