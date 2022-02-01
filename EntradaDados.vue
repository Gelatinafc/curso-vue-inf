<template>
  <input
     @keyup="$emit('input', valorInterno)" 
     v-model="valorInterno"
     type="text" 
     @keyup.enter="$emit('salvar')" 
    />
    
   </template>

<script>
export default {
  props: ["valor"],
  data() {
    return {
      valorInterno: this.valor,
    };
  },
};
</script>

<style>
input {
  margin: 6px;
}
</style>
