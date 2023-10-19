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



<template>
   <form @submit="submit" className="form"> 
    <input  required placeholder="title" v-model="title"  />
    <input required placeholder="description" v-model="description"  />
    <button className="btn" type="submit">Submit</button>
   </form>

</template>

  
<style scoped>
.btn{
    padding: 10px 20px;
    border-radius: 5px;
    border: 3px solid rgb(35, 6, 6);
}

.form{
    display: flex;
    max-height: 30px;
    justify-content: center;
    gap: 8px;
    width: 50px;
    flex-wrap: wrap;
    max-width: 400px;
}

</style>

