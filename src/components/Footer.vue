<template>
  <div class="container">
    <div class="header">
      <div class="ball">
        <img class="img-ball" width="30%" src="/images/ball.png" alt="cat" />
      </div>
      <div class="img-ball">
        <img width="70%" src="/images/pokeapi.png" alt="cat" />
      </div>
      <div class="footer-Made">
        <h6 class="poke-font">Made by</h6>
        <h6 class="poke-font">Camila</h6>
        <h6 class="poke-font">Ardila Plazas</h6>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
@font-face {
  font-family: Pokemon GB;
  src: url("font/Pokemon GB.ttf") format("ttf");
  font-style: Regular;
  font-weight: normal;
}

.poke-font {
  font-family: Pokemon GB;
  font-size: 10px;
  text-align: start;
  color: #ffcb2b;
}

.footer-Made {
  padding: 0px 0px 0px 257px;
}

.header {
  display: flex;
  padding: 0px 0px 0px 80px;
  margin: 69px 0px 0px 0px;
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