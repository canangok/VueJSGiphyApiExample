<template>
  <div class="search">
    <input  class="" type="text" v-model="query" @keypress.enter="handleSearch"/>
    <button @click="handleSearch">Search</button>
  </div>
</template>

<script>
export default {
    data(){
        return {
            query : ''
        }
    },
    methods:{
      handleSearch(){
        this.$emit('searchrequest',this.query);
      }
    }
}
</script>

<style>
  .search input{
    padding: 10px 20px;
    border:1px solid #CCC;
    border-radius: 5px;
    width: 400px;
  }
  .search button{
    padding: 5px 15 px;
    border:1px solid #CCC;
    border-radius: 5px;
    width: 80px;
    height: 45px;
    background-color:palevioletred;
    color:snow;
  }
</style>