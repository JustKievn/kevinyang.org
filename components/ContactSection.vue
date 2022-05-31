<template>
  <v-container id="section-contact" class="py-16" fluid>
    <v-container class="text-left">
      <div class="display-3 text-center">Contact</div>
      <v-divider class="my-8 mx-16 pb-8" />
      <p class="teal-indent">
        Interested in contacting me? Please either send me a message on LinkedIn
        or shoot me an email.
      </p>
      <div>
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
      </div>
    </v-container>
  </v-container>
</template>
<style scoped>
.teal-indent {
  border-left: 4px solid #66fcf1;
  padding-left: 12px;
}
</style>
