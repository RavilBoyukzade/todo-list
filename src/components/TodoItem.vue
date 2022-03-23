<template>
  <div>
    <li>
       <span>
           <input type="checkbox" >
           <strong>{{todo.id}}</strong>
           {{todo.title}}
       </span>
       <button>&times;</button>
    </li>
  </div>
</template>

<script>
export default {
    props:{
        todo:{
            type:Object,
            required:true
        }
    }
}
</script>

<style scoped>
  li{
    border:1px solid black;
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    padding: 10px 20px;
  }
  button{
    color: brown;
    border-radius: 30px;
    border:white;
    background-color: white;
  }

</style>