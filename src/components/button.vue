<template>
    <button class="btn m-3" :class='btnClass'  @click="onPress">{{name}}</button>
</template>

<script>
export default {
  name: 'Button',
  props: ['name', 'btnClass'],
  methods: {
    onPress(){
      this.$emit('onPress');
    }
  }

 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.shadow{
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
