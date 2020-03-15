<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons"
      rel="stylesheet">
    <Header />
    <div class="container">
      <router-view/>
    </div>    
  </div>
</template>

<script>
import Header from './components/layout/Header';
export default {
  name: "app",
  components: {
    Header,
  }
}
</script>


<style lang="stylus">
// $ruler: 16px;
// $color-red: #AE1100;
// $color-bg: #EBECF0;
// $color-shadow: #BABECC;
// $color-white: #FFF;

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
  line-height: 1.4;
  background: #EBECF0;
}

button, input {
  border: 0;
  outline: 0;
  font-size: 16px;
  border-radius: 50px;
  padding: 16px;
  background-color:#EBECF0;
  text-shadow: 1px 1px 0 #fff;
}

input[type="text"] {
  margin-right: 16px/2;
  box-shadow:  inset 2px 2px 5px #BABECC, inset -5px -5px 10px #fff;
  width: 100%;
  box-sizing: border-box;
  transition: all 0.2s ease-in-out;
  appearance: none;
  -webkit-appearance: none;

  &:focus {
    box-shadow:  inset 1px 1px 2px #BABECC, inset -1px -1px 2px #fff;
  }
}

button {
  color:#61677C;
  font-weight: bold;
  box-shadow: -5px -5px 20px #FFF,  5px 5px 20px #BABECC;
  transition: all 0.2s ease-in-out;
  cursor: pointer;
  font-weight: 600;
  
  &:hover {
    box-shadow: -2px -2px 5px #FFF, 2px 2px 5px #BABECC;
  }
  
  &:active {
    box-shadow: inset 1px 1px 2px #BABECC, inset -1px -1px 2px #FFF;
  }
  
  .icon {
    margin-right: 32px;
  }
  
  &.unit {
    border-radius: 32px;
    line-height: 0;
    // width: 16px*3;
    // height: 16px*3;
    display:inline-flex;
    justify-content: center;
    align-items:center;
    margin: 0;
    font-size: 16px*1.2;
    
    .icon {
      margin-right: 0; 
    }
  }
}

  .container {
    max-width: 800px;
    margin: 50px auto;
    padding: 0 15px;
  }
</style>
