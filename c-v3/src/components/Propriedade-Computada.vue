<template>

<div class="cl"> 
    {{ fullname }} <br><br>

<h2>Todos em aberto</h2> <br>

<div v-for="todo in uncompletedTodos" :key="todo.id">

{{ todo.title }} <span>{{ todo.completed }}</span>

</div> <br>

<h2>Todos completas</h2> <br>
<div v-for="todo in completedTodos" :key="todo.id">

{{ todo.title }} <span>{{ todo.completed }}</span>

</div> <br>

<h2>TODOS</h2> <br>

<div v-for="todo in todos" :key="todo.id">

<input v-model="todo.completed" type="checkbox">

{{ todo.title }} <span>{{ todo.completed }}</span>

</div>

</div>

</template>

<script>

export default {
    data() {
        return {
            user: {
                firstname: 'Jonh',
                lastname: 'Snow',
            },
            todos: [
  {
    "userId": 1,
    "id": 1,
    "title": "delectus aut autem",
    "completed": false
  },
  {
    "userId": 1,
    "id": 2,
    "title": "quis ut nam facilis et officia qui",
    "completed": false
  },
  {
    "userId": 1,
    "id": 3,
    "title": "fugiat veniam minus",
    "completed": false
  },
  {
    "userId": 1,
    "id": 4,
    "title": "et porro tempora",
    "completed": true
  },
]
        }
    },
    computed: {
        fullname() {
           return `${this.user.firstname} ${this.user.lastname}`
        },
        uncompletedTodos() {
            return this.todos.filter(todo => !todo.completed);
        },
        completedTodos() {
            return this.todos.filter(todo => todo.completed);
        }
    },
    methods: {
        Click() {
            console.log(this);
        }
    }
}
  

</script>

<style scoped>
.cl {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 100px;
    flex-direction: column;
    
}



</style>

