<template>
  <div>
    <h2>{{title}}</h2>
    <button @click="updateTitle()">Add new list</button>
  </div>
</template>

<script>
export default {
  name:'childItem',
  props:{
    title:String
  },

  methods:{
    updateTitle(){
      this.$emit('updateTitle','Add more items');
    },
  },
};
</script>