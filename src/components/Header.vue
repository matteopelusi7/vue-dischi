<template>
  <header>
    <figure class="logo">
      <img src="../assets/img/logo.svg" alt="">
    </figure>
  </header>
</template>

<script>
export default {
  name: 'MainContent',
  
}
</script>

<style scoped lang="scss">

header {
  background-color: #2e3a46;
  height: 60px;
  display: flex;
  align-items: center;
  padding-left: 10px;

  .logo {
    width: 110px;
  }

}

</style>
