<template>
<div class="main">
    <div class="card">
      <h1>Simple Counter App</h1>
      <h2>{{count}}</h2>
      <div class="btncontainer">
          <Button name="Add" btnClass="btn-primary" @onPress="add" />
          <Button name="Subtract" btnClass="btn-danger" @onPress="subtract" />
      </div>
    </div>
</div>
</template>

<script>
import Button from './button.vue';

export default {
  name: 'Counter',
  props: [],
   components: {
    Button
  },
  data(){
    return{
      count: 0
    }
  },
  methods: {
    add(){
      this.count = this.count + 1 
    },
    subtract(){
      this.count = this.count - 1  
    }
  }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main{
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.card{
  background-color: #cacaca;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.btncontainer{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

h1{
  color: blue;
}
</style>
