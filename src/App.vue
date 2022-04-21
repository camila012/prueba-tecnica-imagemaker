<template>
  <div id="app">
    <div>
      <Header />
    </div>
    <div>
      <Content />
    </div>
    <div>
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Content from "./components/Content";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    Header,
    Content,
    Footer,
  },
};
</script>

<style>
#app {
  text-align: center;
}
</style>
