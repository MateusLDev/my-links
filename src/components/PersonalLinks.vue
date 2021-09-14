<template>
  <div class="links-list d-flex flex-column mt-6 mx-4">
    <div
      class="link-list px-4 py-2 mb-4"
      v-for="item in personalLinks"
      :key="item.id"
    >
      <a :href="item.url">{{ item.text }}</a>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

import PersonalLinksInterface from '@/types/personalLinks';

@Component({})
export default class PersonalLinks extends Vue {
  @Prop({ type: Array, required: true })
  personalLinks!: PersonalLinksInterface[];
}
</script>
<style scoped>
.link-list {
  border: 1px solid #868686;
  border-radius: 20px;
}

.link-list a {
  color: #000;
  text-decoration: none;
}
</style>
