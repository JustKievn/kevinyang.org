<template>
  <v-navigation-drawer app>
    <div class="text-center my-6">
      <v-img src="/img/mug_icon.png" class="ma-2" height="60" contain />
      <p class="display-1 mb-1">Kevin Yang</p>
      <p class="title">Full-Stack Developer</p>
    </div>
    <v-divider class="my-1 mx-4"></v-divider>
    <v-list class="text-center" dense nav>
      <v-list-item link @click="scrollTo('#section-landing')">
        <v-list-item-content>
          <v-list-item-title>
            <v-icon>mdi-home</v-icon>
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-list-item
        v-for="page in navigation"
        :key="page.text"
        link
        @click="scrollTo(page.to)"
      >
        <v-list-item-content>
          <v-list-item-title>{{ page.text }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
    <v-spacer />
    <template #append>
      <v-divider class="my-1 mx-4"></v-divider>
      <div class="text-center my-6">
        <v-btn fab small class="mx-1">
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn fab small class="mx-1">
          <v-icon>mdi-email</v-icon>
        </v-btn>
        <v-btn fab small class="mx-1">
          <v-icon>mdi-github</v-icon>
        </v-btn>
      </div>
    </template>
  </v-navigation-drawer>
</template>
<script>
export default {
  data() {
    return {
      navigation: [
        {
          text: 'About',
          to: '#section-about',
        },
        {
          text: 'Skills',
          to: '#section-skills',
        },
        {
          text: 'Experience',
          to: '#section-experience',
        },
        {
          text: 'Contact',
          to: '#section-contact',
        },
      ],
    }
  },
  methods: {
    scrollTo(target) {
      this.$vuetify.goTo(target, {})
    },
  },
}
</script>
