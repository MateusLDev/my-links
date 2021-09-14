<template>
  <div class="person-social d-flex justify-space-around">
    <div v-for="item in socialMedias" :key="item.id">
      <a :href="item.url" target="_blank">
        <v-icon>{{ item.icon }}</v-icon>
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

import SocialMediasInterface from '@/types/socialMedias';
@Component({})
export default class SocialMedias extends Vue {
  @Prop({ type: Array, required: true })
  socialMedias!: SocialMediasInterface[];
}
</script>
<style scoped>
.person-social {
  margin: 0 auto;
  width: 200px;
}

.person-social a {
  color: none;
  text-decoration: none;
}
</style>
