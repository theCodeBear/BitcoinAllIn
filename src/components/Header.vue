<template>
  <section>
    <img id='logo' alt='bitcoin picture' src='../assets/bitcoinImage.png' v-on:click="menuItemClick('Home')" />
    <div id='title'>
      <!-- <div style='font-size: 32px; margin-bottom: 10px;'>Bitcoin All In!</div> -->
      <h1>Bitcoin All In!</h1>
      <div class='subheader'>A tkrone project</div>
    </div>
    <nav id='menu'>
      <span v-on:click="menuItemClick(item)" v-for="item in menuItems">
        {{item}}
      </span>
    </nav>
  </section>
</template>


<script>
  export default {
    data() {
      return {
        menuItems: [
          "What is Bitcoin?",
          "Charts",
          "Articles",
          "History",
          "About"
        ]
      }
    },
    methods: {
      menuItemClick(menuItem) {
        this.$emit('change-content', menuItem)
      }
    }
  }
</script>


<style>
section {
  width: 100%;
  height: 100px;
  background-color: black;
  text-align: left;
}
#logo {
  height: 100px;
}
#title {
  display: inline-block;
  padding: 0 30px 0 30px;
  vertical-align: top;
  height: 100%;
  color: white;
}
h1 {
  margin-top: 0;
  font-size: 2em;
  font-weight: normal;
}
.subheader {
  font-size: 0.9em;
}
#menu {
  display: flex;
  justify-content: space-around;
}
#menu span {

}
</style>
