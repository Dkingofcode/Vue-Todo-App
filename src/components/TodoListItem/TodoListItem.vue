<template>
   <div className="form-input">
     <input type="checkbox" :value="todo.isChecked">
     <span>
       <strong>{{todo.title}}</strong> 
     </span>
     <span style="margin: 0 20px">
      {{todo.description}}  
     </span>
   </div> 
</template>

<script lang="ts">
  export default {
    name: "TodoListItem",
    props: {
       todo: {
          type: Object,
          required: true 
       }, 
    },

  computed: {
    isChecked: {
      get() {
         return this.todo.isChecked
      },
      set(value){
        console.log(value);
      }  
    }
  },  

  methods: {
    toggleIsChecked(event){
        console.log(event.target.value);
    }
  },
}
</script>

<style scoped>


</style>


