<template>
  <header>
      <h1><center>{{ valor }}</center></h1>
  </header>
</template>

<script>
export default {
props: ["valor"],

};
</script>

<style >
header {
   background-color: blue;
   height: 28px;
   width: 1400px;
}
   



</style>