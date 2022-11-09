<template>
  <form @submit.prevent="create(item)">
    <input v-model="item" placeholder="ToDo Item" />
    <button>Create</button>
  </form>
</template>

<script>
import { ref } from 'vue';

export default {
  props: {
    createItem: {
      type: Function,
      require: true,
    },
  },
  setup(props) {
    const item = ref('');

    function create() {
      if (item.value) {
        props.createItem(item.value);
        item.value ='';
      }
    }

    return {
      item,
      create,
    };
  },
};
</script>

<style scoped></style>
