<template>
  <div class="todolist">
    <input type="text" class="todo-input" placeholder="What needs to be done?" v-model="newTodo" @keyup.enter="addToDo"/>
    <div v-for="todo in todos" :key="todo.id" class="todo-item">
        {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  data() {
      return {
          newTodo: '',
          todos: [
              {
                  id: 1,
                  title: 'Finish Screen Cast',
                  completed: false,
              },
              {
                  id: 2,
                  title: 'Take Over World',
                  completed: false,
              },
          ]
      }
  },
  methods: {
      addToDo() {
        this.todos.push({
            id: this.idForTodo,
            title: this.newTodo,
            completed: false,
        })

        this.newTodo = ''
        this.idForTodo++
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.todo-input {
    width: 100%;
    padding: 10px 10px;
    font-size: 18px;
    margin-bottom: 16px;

    &:focus {
        outline: 0
    }
}
</style>
