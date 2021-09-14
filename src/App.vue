<template>
  <v-app id="links-wrapper">
    <v-container>
      <v-main>
        <v-card class="card-links mx-auto elevation-10" max-width="400px">
          <v-img height="130" src="@/assets/bg-pattern-card.svg"></v-img>
          <v-avatar class="person-image ml-auto" size="90">
            <v-img src="@/assets/image-victor.jpg"></v-img>
          </v-avatar>
          <v-card-title class="person-name justify-center mt-8"
            >Mateus Lopes, <span class="person-age"> 19</span></v-card-title
          >
          <v-card-subtitle class="person-profession d-flex justify-center"
            >Frontend Developer</v-card-subtitle
          >
          <div class="person-social d-flex justify-space-around">
            <a href="https://github.com/MateusLDev">
              <v-icon>mdi-github</v-icon>
            </a>
            <a href="https://www.instagram.com/mtszc/">
              <v-icon>mdi-instagram</v-icon>
            </a>
            <a href="https://www.twitch.tv/mxteuslopxes">
              <v-icon>mdi-twitch</v-icon>
            </a>
          </div>
          <div class="links-list d-flex flex-column mx-4">
            <a class="link-list px-4 py-2 mb-4">aaaa</a>
            <a class="link-list px-4 py-2">bbb</a>
          </div>
        </v-card>
      </v-main>
    </v-container>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
@Component({})
export default class App extends Vue {}
</script>
<style>
#links-wrapper {
  background: linear-gradient(
    60deg,
    rgba(25, 162, 174, 1) 19%,
    rgba(124, 129, 148, 1) 88%
  );
  width: 100%;
  height: 100vh;
}

.card-links {
  border-radius: 12px !important;
}

.person-image {
  position: absolute !important;
  border: 4px solid #fff;
  top: 85px;
  left: 155px;
}

.person-name {
  font-family: 'Kumbh Sans', sans-serif;
  font-weight: 700 !important;
}

.person-age {
  color: rgba(0, 0, 0, 0.6);
  font-family: 'Kumbh Sans', sans-serif;
  font-weight: 500 !important;
}

.person-social {
  margin: 0 auto;
  width: 200px;
}

.person-social a {
  color: none;
  text-decoration: none;
}

.link-list {
  border: 1px solid #868686;
  border-radius: 20px;
}

.text-center {
  text-align: center !important;
}
</style>
