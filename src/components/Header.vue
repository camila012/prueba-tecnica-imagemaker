<template>
  <div class="container">
    <div class="header">
      <div class="ball">
        <img class="img-ball" width="30%" src="/images/ball.png" alt="cat" />
      </div>
      <div class="img-ball">
        <img width="70%" src="/images/pokeapi.png" alt="cat" />
      </div>
      <div class="ball">
        <img class="img-ball" width="30%" src="/images/ball.png" alt="cat" />
      </div>
    </div>
  </div>
</template>

<style>
@font-face {
  font-family: Pokemon GB;
  src: url("font/Pokemon GB.ttf") format("ttf");
  font-style: Regular;
  font-weight: normal;
}

body {
  background-color: #ff1c1c;
  margin: 0px 0px 0px 0px;
}

.poke-font {
  font-family: Pokemon GB;
}

.header {
  display: flex;
  padding: 0px 0px 0px 80px;
  margin: 0px 0px 0px 0px;
  background-color: #000;
  height: 7rem;
}

.ball {
  padding: 0px 75px 0px 0px;
}

.img-ball {
  margin: -40px 0px 0px 0px;
}
</style>