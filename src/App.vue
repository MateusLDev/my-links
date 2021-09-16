<template>
  <v-app id="links-wrapper" class="d-flex justify-center">
    <img src="@/assets/bg-pattern-top.svg" class="pattern-top" />
    <img src="@/assets/bg-pattern-bottom.svg" class="pattern-bottom" />
    <v-container>
      <v-main>
        <v-card class="card-links mx-auto pb-6 elevation-10" max-width="380px">
          <v-img height="130" src="@/assets/bg-pattern-card.svg"></v-img>
          <v-avatar class="person-image ml-auto" size="90">
            <v-img
              src="@/assets/image-victor.jpg"
              alt="Mateus Profile Pic"
            ></v-img>
          </v-avatar>
          <v-card-title class="person-name justify-center mt-8"
            >Mateus Lopes, <span class="person-age"> 19</span></v-card-title
          >
          <v-card-subtitle class="person-profession d-flex justify-center"
            >Frontend Developer</v-card-subtitle
          >
          <SocialMedias :socialMedias="socialMediaItems" />
          <PersonalLinks :personalLinks="personalLinkItems" />
        </v-card>
      </v-main>
    </v-container>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

import SocialMedias from '@/components/SocialMedias.vue';
import PersonalLinks from '@/components/PersonalLinks.vue';

import SocialMediasInterface from '@/types/socialMedias';
import PersonalLinksInterface from '@/types/personalLinks';

@Component({
  components: {
    SocialMedias: SocialMedias,
    PersonalLinks: PersonalLinks,
  },
})
export default class App extends Vue {
  socialMediaItems: SocialMediasInterface[] = [
    { url: 'https://github.com/MateusLDev', icon: 'mdi-github' },
    { url: 'https://www.instagram.com/mtszc/', icon: 'mdi-instagram' },
    { url: 'https://www.twitch.tv/mxteuslopxes', icon: 'mdi-twitch' },
  ];

  personalLinkItems: PersonalLinksInterface[] = [
    { url: 'https://github.com/MateusLDev', text: 'Portfolio' },
    { url: 'https://github.com/MateusLDev', text: 'Pingback' },
    { url: 'https://www.instagram.com/mtszc/', text: 'Desbugando.dev' },
  ];
}
</script>
<style>
@font-face {
  font-family: 'Kumbh Sans';
  src: url('./assets/fonts/KumbhSans-Regular.ttf') format('opentype');
}

@font-face {
  font-family: 'Kumbh Sans Medium';
  src: url('./assets/fonts/KumbhSans-Medium.ttf') format('opentype');
}

@font-face {
  font-family: 'Kumbh Sans Bold';
  src: url('./assets/fonts/KumbhSans-Bold.ttf') format('opentype');
}

html {
  overflow: hidden;
  box-sizing: border-box;
}

#links-wrapper {
  background: linear-gradient(
    60deg,
    rgba(25, 162, 174, 1) 19%,
    rgba(124, 129, 148, 1) 88%
  );
  width: 100%;
}

.pattern-top {
  width: 60%;
  position: absolute;
  top: -400px;
  left: -200px;
  overflow: hidden;
}

.pattern-bottom {
  width: 60%;
  position: absolute;
  bottom: -400px;
  right: -200px;
  overflow: hidden;
}

.card-links {
  border-radius: 12px !important;
}

.person-image {
  position: absolute !important;
  border: 4px solid #fff;
  top: 85px;
  left: calc(50% - 43px);
}

.person-name {
  font-family: 'Kumbh Sans Bold', sans-serif;
  font-weight: 700 !important;
}

.person-age {
  color: rgba(0, 0, 0, 0.6);
  font-family: 'Kumbh Sans Medium', sans-serif;
  font-weight: 500 !important;
}

.w-100 {
  width: 100% !important;
}
</style>
