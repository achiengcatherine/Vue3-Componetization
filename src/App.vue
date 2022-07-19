<template>
  <div id="app" >
<child @updateTitle="updateTitle($event)" v-bind:title="title"></child>
    <ul type="none">
      <li>stationery</li>
      <li>food items</li>
      <li>clothes</li>
    </ul>
  </div>
</template>

<script>
import child from "@/components/child.vue";
export default {
  name: 'App',
  components: {
    child
  },
  data() {
    return {
      title: 'My shopping list'
    }
  },

  methods:{
    updateTitle(title){
      this.title=title
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
