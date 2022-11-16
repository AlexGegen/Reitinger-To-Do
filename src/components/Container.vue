<template>
  <div class="container">
    <Create :createItem="createItem" />
  </div>
</template>

<script>
import { ref } from 'vue';
import Create from './CreateItem.vue';

export default {
  components: {
    Create,
  },

  setup() {
    let data = ref(
      { name: 'Eating' },
      { name: 'Drinking' },
      { name: 'Sleeping' }
    );

    function createItem(item) {
      console.log('Create Item ...' + item);
      data.push(item);
    }

    return {
      data,
      createItem,
    };
  },
};
</script>
