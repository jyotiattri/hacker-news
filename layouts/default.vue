<template>
  <div class="container">
    <AppHeader/>
    <nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader';

export default {
  components: {
    AppHeader
  }
  
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  background: #fff;
}

a {
  color: #666;
  text-decoration: none;
}

ul {
  list-style: none;
}

.container {
width: 85%;
 margin: 0 auto;
  display: flex;
background: #f6f6ef;
}

</style>
