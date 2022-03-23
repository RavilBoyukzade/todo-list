<template>
  <div>
    <li>
       <span>
           <input type="checkbox" >
           <strong>{{todo.id}}</strong>
           {{todo.title}}
       </span>
       <button class="btn-delete">&times;</button>
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
.btn-delete{
    color: #dc3545;
    background-color: transparent;
    background-image: none;
    border-color: #dc3545;
    display: inline-block;
    font-weight: 400;
    text-align: center;
    white-space: nowrap;
    vertical-align: middle;
    user-select: none;
    border: 1px solid ;
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    line-height: 1.5;
    border-radius: 50px;
  }
  .btn-delete:hover{
    background-color: #dc3545;
    color:#fff;
  }

</style>