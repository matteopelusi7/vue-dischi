<template>

<div class="select">

   <select name="" id="">
    <option value="">Rock</option>
    <option value="">Pop</option>
    <option value="">Jazz</option>
    <option value="">Metal</option>
  </select>

</div>
  
</template>

<script>
export default {
  name: 'OptionBar',
  
}
</script>

<style scoped lang="scss">

.select {

  margin-bottom: 50px;
  text-align: center;

  select {
    width: 250px;
    padding: 7px 10px;
    color: white;
    border: 1px solid white;
    background-color: #2e3a46;
  }

}

</style>
