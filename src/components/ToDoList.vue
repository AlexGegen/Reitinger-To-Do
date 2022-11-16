<template>
  <div class="container">
    <ul>
      <li v-for="(item, index) in toDoList" :key="index">
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
