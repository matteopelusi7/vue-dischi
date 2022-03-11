<template>

  <div class="select">

    <select name="" id="" v-model="searchInit" @change="$emit('search', searchInit)">
      <option value="All">Tutti</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>

  </div>
  
</template>

<script>
export default {
  name: 'OptionBar',
  data() {
    return {
      searchInit: ''
    }
  }
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
