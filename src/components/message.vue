<template>
  <div class="container content">
    <div class="ball">
      <img class="pokedex" width="20%" src="/images/pokedex.png" alt="cat" />
    </div>
    <a href="" class="ball">
      <img class="ball-content" width="10%" src="/images/ball.png" alt="cat" />
    </a>
  </div>
</template>

<style>
@font-face {
  font-family: Pokemon GB;
  src: url("font/Pokemon GB.ttf") format("ttf");
  font-style: Regular;
  font-weight: normal;
}

.poke-font {
  font-family: Pokemon GB;
}

.pokedex {
  margin: 97px 95px 200px 0px;
}

.ball-content {
  padding: 0px 42px 0px 0px;
}

.content {
  background-color: #273543;
  margin: 42px 0px 34px 0px;
}
</style>