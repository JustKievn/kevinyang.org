<template>
  <v-app id="section-landing">
    <v-row justify="center" align="center">
      <v-col class="text-center" cols="12">
        <div>
          <v-avatar id="avatar" class="mb-4" size="200">
            <img src="/img/profile.jpeg" alt="Kevin" />
          </v-avatar>
        </div>
        <div class="display-2">Kevin Yang</div>
        <div class="title">Software Engineer @ Bloomberg</div>
      </v-col>
    </v-row>
  </v-app>
</template>
<script>
export default {
  data() {
    return {}
  },
}
</script>
<style scoped>
#section-landing {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.6)),
    url('/img/background.jpg');
  background-size: cover;
  background-position: center center;
}
#avatar {
  border: 4px solid #45a29e;
}
</style>
