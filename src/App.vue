<template>
  <div id="app">
    <v-row no-gutters>
      <v-col cols="3">
        <router-link to="/">
          <img
            height="250"
            width="250"
            alt="Les Aliments Crown"
            src="./assets/Logo_LAC.png"
          />
        </router-link>
      </v-col>

      <v-col :cols="$vuetify.breakpoint.mobile ? 1 : 4"></v-col>

      <v-col :cols="$vuetify.breakpoint.mobile ? 2 : 1">
        <v-btn text block to="/"> Home </v-btn>
      </v-col>

      <v-col :cols="$vuetify.breakpoint.mobile ? 2 : 1">
        <v-btn text block to="/contact"> Contact </v-btn>
      </v-col>

      <v-col :cols="$vuetify.breakpoint.mobile ? 2 : 1">
        <v-btn text block to="/services"> Services </v-btn>
      </v-col>

      <v-col :cols="$vuetify.breakpoint.mobile ? 2 : 1">
        <v-btn text block to="/about"> About </v-btn>
      </v-col>
      <v-col>
      </v-col>
      <v-col :cols="$vuetify.breakpoint.mobile ? 2 : 1"></v-col>
    </v-row>

    <router-view />

  </div>
</template>
<script>
export default {
  data() {
    return {
    }
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.theme--light.v-btn--active:hover::before,
.theme--light.v-btn--active::before {
  opacity: 0;
}
.v-btn {
  height: 100px !important;
}
</style>
