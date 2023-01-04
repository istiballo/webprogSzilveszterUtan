<template>
  <v-app>
    <div class="header-container">
      <div class="header">
        <div class="logo-div">
          <div style="background: #fefefe; border-radius: 50%; width: 50px; height: 50px"></div>
        </div>
        <div class="searchFieldContainer">
          <div style="max-width: 300px; position: relative; top: 12px;">
            <v-text-field
            height="30"
            placeholder="Keresés.."
            solo
            dense
            rounded
            background-color="black"
            ></v-text-field>
          </div>
          <v-icon class="menu-button" color="white" x-large>mdi-cart</v-icon>
        </div>
      </div>
    </div>
    <div class="menubar">
            <ul>
              <li>Csokoládék</li>
              <li>Üditők</li>
              <li>Chipsek</li>
            </ul>
      </div>
      <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      app
    >
      <span class="footer">&copy; {{ new Date().getFullYear() }} Designed By István and Alpár</span>
    </v-footer>
  </v-app>
</template>

<script>

import { mapState, mapActions } from 'vuex';


export default {
  name: 'DefaultLayout',
}
</script>

<style scoped>
.footer{
  margin: 0 auto;
}
.menubar{
  width: 100%;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #696969;
  border-top: 1px solid black;
}
ul li{
  display: inline;
  padding: 2em;
  font-size: 1.5em;
}
.header {
  width: 80%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  position: relative;
}

.searchFieldContainer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-div {
  position: absolute;
  top: 50%;
  left: 10%;
  transform: translate(-50%,-50%);
}

.header-container {
  width: 100%;
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #696969;
}

.menu-button {
  cursor: pointer;
}
</style>