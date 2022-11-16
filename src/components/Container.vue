<template>
  <div class="container">
    <Create :createItem="createItem" />
    <ToDoList :toDoList="data" />
  </div>
</template>

<script>
import { ref } from 'vue';
import Create from './CreateItem.vue';
import ToDoList from './ToDoList.vue';

export default {
  components: {
    Create,
    ToDoList
  },

  setup() {
    let data = ref([
      { name: 'Eating' },
      { name: 'Drinking' },
      { name: 'Sleeping' }
    ]);

    function createItem(item) {
      console.log('Create Item ...' + item);
      if (!data.value.includes(item)) data.value.push(item);
    }

    return {
      data,
      createItem,
    };
  },
};
</script>
