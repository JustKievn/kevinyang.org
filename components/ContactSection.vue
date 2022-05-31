<template>
  <v-container id="section-contact" class="py-16" fluid>
    <v-container class="text-left">
      <div class="display-3 text-center">Contact</div>
      <v-divider class="my-8 mx-16 pb-8" />
      <p class="text-center">
        Interested in contacting me?<br />
        Feel free to reach out to me on LinkedIn or send me an email at the
        links below:
      </p>
      <table class="ma-auto pt-4">
        <tr height="50">
          <td>
            <v-btn
              fab
              small
              class="mx-1 _darkteal mr-4"
              :href="$store.state.me.linkedin_url"
              target="_blank"
            >
              <v-icon>mdi-linkedin</v-icon>
            </v-btn>
          </td>
          <td>
            {{ $store.state.me.linkedin_url }}
          </td>
        </tr>
        <tr height="50">
          <td>
            <v-btn
              fab
              small
              class="mx-1 _darkteal mr-4"
              :href="`mailto:` + $store.state.me.email"
            >
              <v-icon>mdi-email</v-icon>
            </v-btn>
          </td>
          <td>
            {{ $store.state.me.email }}
          </td>
        </tr>
      </table>
    </v-container>
  </v-container>
</template>
