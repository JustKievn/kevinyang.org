<template>
  <v-container id="section-experience" class="py-16" fluid>
    <v-container class="text-left">
      <div class="display-3 text-center">Experience</div>
      <v-divider class="my-8 mx-16 pb-8" />
      <v-timeline>
        <v-timeline-item
          v-for="(item, key) in timeline"
          :key="key"
          color="_teal"
        >
          <div slot="opposite" v-for="t in item.time" :key="t">{{t}}</div>
          <v-card class="elevation-2">
            <v-card-title class="text-h5">
              {{ item.position }} <v-spacer /> {{ item.company }}
            </v-card-title>
            <v-card-text v-show="item.text">
              {{ item.text }}
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-container>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      timeline: [
        {
          position: 'Software Engineer 3',
          company: 'Comcast',
          text: 'Worked on a series of web applications to assist/automate several aspects of network engineering',
          time: ['(SWE 3) March 2021 - Present', '(SWE 2) Jun 2019 - March 2021'],
        },
        {
          position: 'Software Engineer Co-op',
          company: 'Comcast',
          text: "Created scripts to parse and store information on Comcast's L2 Network",
          time: ['Sep 2016 - June 2019'],
        },
        {
          position: 'Info Systems Specialist',
          company: 'LSAC',
          time: ['Sep 2015 - March 2016'],
        },
      ],
    }
  },
}
</script>
