<template>
  <v-app id="links-wrapper">
    <v-container>
      <v-main>
        <v-card class="card-links mx-auto pb-6 elevation-10" max-width="380px">
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
    { url: 'https://github.com/MateusLDev', text: 'aaa' },
    { url: 'https://www.instagram.com/mtszc/', text: 'bbb' },
    { url: 'https://www.twitch.tv/mxteuslopxes', text: 'ccc' },
  ];
}
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
  left: 148px;
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
</style>
