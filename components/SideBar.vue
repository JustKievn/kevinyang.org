<template>
  <v-navigation-drawer app>
    <div class="text-center my-6">
      <v-img src="/img/mug_icon.png" class="ma-2" height="60" contain />
      <p class="display-1 mb-1">Kevin Yang</p>
      <p class="title">Full-Stack Developer</p>
    </div>
    <v-divider class="my-1 mx-4"></v-divider>
    <v-list class="text-center" dense nav>
      <v-list-item link @click="goHome()">
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
        <v-btn
          fab
          small
          class="mx-1"
          :href="$store.state.me.linkedin_url"
          target="_blank"
        >
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn fab small class="mx-1" :href="`mailto:` + $store.state.me.email">
          <v-icon>mdi-email</v-icon>
        </v-btn>
        <v-btn
          fab
          small
          class="mx-1"
          :href="$store.state.me.github_url"
          target="_blank"
        >
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
    goHome() {
      if (window.location.pathname === '/') {
        if (window.pageYOffset > 0) {
          this.scrollTo('#section-landing')
        }
      } else {
        window.location.href = '/'
      }
    },
    scrollTo(target) {
      this.$vuetify.goTo(target, {})
    },
  },
}
</script>
