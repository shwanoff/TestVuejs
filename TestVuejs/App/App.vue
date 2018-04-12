<template>
  <div id="home">
    <nav>
      <ul>
        <li>text 1</li>
        <li>text 2</li>
      </ul>
    </nav>
    <h1>Hello World!</h1>
    <h2>Привет, мир!</h2>
    <ul>
      <li>text 3</li>
      <li>text 4</li>
    </ul>
    <div class="box">
      hello
    </div>
    <div class="success">OK</div>
    <div class="error">Error</div>
    <div class="marg">Отступ</div>
    <div class="wid">Светофор</div>
  </div>
</template>

<script>
  export default { }
</script>

<style lang="scss">
  @import './variables.scss';

  nav {
  ul {
  margin: 0;
  padding: 0;
  color: red;
  list-style: none;
  }

  li { display: inline-block; }
  }

  h1 {
  color: $blue;
  }

  @import '_h2partial';

  @mixin border-r($radius) {
  -webkit-border-radius: $radius;
  -moz-border-radius: $radius;
  -ms-border-radius: $radius;
  border-radius: $radius;
  }

  .box {
  @include border-r(10px);
  border-style: solid;
  max-width: 100px;
  }

  .message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
  }

  .success {
  @extend .message;
  border-color: green;
  }

  .error {
  @extend .message;
  border-color: red;
  }

  .marg {
  margin-left: 100px + 20px;
  padding-top: 10% + 5%;
  }

  $width: 150px;
  .wid {
  @if($width < 200) {
      color: red;
    }
    @else if ($width > 700) {
      color: green;
    }
    @else {
      color: yellow;
    }
    
    width: $width;
  }
</style>