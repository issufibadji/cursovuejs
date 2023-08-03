<template>
    <header class="header">
        <a href="#default" class="logo">Logo</a>
        <div class="header-right">
          <a class="active" href="#home">Home</a>
          <a href="#contact">Contact</a>
          <a href="#about">Ajuda</a>
      </div>
    </header>
</template>

<script>
    export default {

    }
</script>

<style>
* {box-sizing: border-box;}
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
    .header {
      position: fixed;
      left: 0;
      top: 0;
      width: 100%;
      background-color: dodgerblue;
      color: white;
      text-align: center;
    }



    .header a {
      float: left;
      color: black;
      text-align: center;
      padding: 12px;
      text-decoration: none;
      font-size: 18px;
      line-height: 25px;
      border-radius: 4px;
    }

    .header a.logo {
      font-size: 25px;
      font-weight: bold;
    }

    .header a:hover {
      background-color: #ddd;
      color: black;
    }

    .header a.active {
      background-color: blue;
      color: white;
    }

    .header-right {
      float: right;
    }

    @media screen and (max-width: 500px) {
      .header a {
        float: none;
        display: block;
        text-align: left;
      }

      .header-right {
        float: none;
      }
    }

</style>
