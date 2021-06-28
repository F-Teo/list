<template>
    <ul class='w-96 h-80 overflow-y-scroll  position bg'>
      <ListItem
        v-for="item in list"
        v-bind:list="item"
        v-bind:key="item.index"
      />
    </ul>
</template>

<script>
import ListItem from './ListItem.vue';

export default {
  props: ["list"],
  components: {
    ListItem,
  },
};
</script>

<style  scoped>
    .position {
        margin: 2.5rem auto;
    }
    .bg {
        background-color: #092740;
    }
    ul {
      scrollbar-width: thin;
      scrollbar-color: #316694 #092740;
    }

    ul::-webkit-scrollbar {
    width: 12px;               
    }

    ul::-webkit-scrollbar-track {
    background: #092740;      
    }

    ul::-webkit-scrollbar-thumb {
    background-color: #316694;   
    border-radius: 10px;      
    border: 1px solid #316694;  
    }
</style>