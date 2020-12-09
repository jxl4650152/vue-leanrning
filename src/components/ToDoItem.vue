<template>
  <div>
    <input type="checkbox" :id="id" :checked="isDone" />
    <label for="todo-item">{{ label }}</label>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        isDone: this.done,
      };
    },

    props: {
      label: {
        required: true,
        type: String
      },
      done: {
        default: false,
        type: Boolean
      },
      id: {
        required: true,
        type: String
      }
    }
  };
</script>
