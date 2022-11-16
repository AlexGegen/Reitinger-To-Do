<template>
  <div class="container">
    <ul>
      <li v-for="(item, index) in toDoLost" :key="index">
        {{ item.name }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
props:{
    toDoList:{
      type: Array,
      required: true,
    },
},

setup(){
  return{};
},
}
</script>
