<template>
  <div class="todolist">
    <input type="text" class="todo-input" placeholder="What needs to be done?"/>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  props: {
    msg: String
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
