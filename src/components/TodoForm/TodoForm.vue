<template>
   <form @submit="submit"> 
    <input  required placeholder="title" v-model="title"  />
    <input required placeholder="description" v-model="description"  />
    <button type="submit"></button>
   </form>

</template>

  <script lang="ts">
   export default {
     name: "Todoform",

     data() {
        return {
          title: '',
          description: ""
        }
     },

     methods: {
        submit(){
            console.log(this.state)
            console.log(this.description)
            console.log('hey')
        }
     }
   }

  </script>

<style scoped>



</style>

