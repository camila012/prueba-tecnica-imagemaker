<template>
  <div class="container content">
    <div class="ball">
      <img class="pokedex" width="20%" src="/images/pokedex.png" alt="cat" />
    </div>
    <div class="pikachu-content" v-if="show">
      <div class="title-content">
        <h1 class="poke-font-content">
          {{ name }} &nbsp;&nbsp; # <b>{{ id }}</b>
        </h1>
      </div>
      <div class="content-ball">
        <img class="pikachu-color" :src="image" width="30%" />
        <div class="content-api">
          <p class="poke-font-content">
            HP: <b>{{ hp }}</b> - attack: <b>{{ attack }}</b>
          </p>
          <p class="poke-font-content weight">
            Weight: <b>{{ weight }}</b> kg
          </p>
          <p class="poke-font-content">Ability : {{ ability }}</p>
        </div>
      </div>
    </div>
    <img
      @click="contentBall()"
      class="ball-content"
      width="10%"
      src="/images/ball.png"
      alt="cat"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: true,
      name: "",
      id: "",
      image: "",
      hp: "",
      weight: "",
      ability: "",
      attack: "",
    };
  },
  methods: {
    contentBall() {
      const url = "https://pokeapi.co/api/v2/pokemon/pikachu";
      fetch(url)
        .then((res) => {
          return res.json();
        })
        .then((data) => {
          this.id = data.id;
          this.name = data.name;
          this.image = data.sprites.other.home.front_default;
          this.hp = data.stats[0].base_stat;
          this.attack = data.stats[1].base_stat;
          this.weight = data.weight;
          this.ability = data.types[0].type.name;
        })
        .catch((err) => {
          console.log(err);
        });
      this.show = !this.show;
    },
  },
};
</script>

<style>
@font-face {
  font-family: Pokemon GB;
  src: url("font/Pokemon GB.ttf") format("ttf");
  font-style: normal;
  font-weight: normal;
}

.poke-font-content {
  font-family: Pokemon GB;
  font-size: 20px;
  color: #fff;
  padding: 20px;
}

.pikachu-color {
  background-color: #fff;
  border-radius: 30px;
}

.weight {
  padding: 0px 102px 0px 0px;
}

.content-ball {
  display: flex;
  padding: 38px 0px 46px 52px;
}

.content-api {
  padding: 25px 0px 0px 42px;
}

.pokedex {
  margin: 97px 0px 200px 84px;
}

.ball-content {
  padding: 0px 0px 74px 6px;
}

.content {
  background-color: #273543;
  margin: 72px 0px 34px 0px;
}

.pikachu-content {
  border: 12px solid black;
  background-color: #ff1c1c;
  width: 50%;
  border-radius: 50px;
  margin: 0px 0px -102px 506px;
}

.title-content {
  border-bottom: 12px solid black;
  padding: 20px;
}
</style>

