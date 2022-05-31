<template>
  <v-container id="section-skills" class="py-16" fluid>
    <v-container class="text-left">
      <div class="display-3 text-center">Skills</div>
      <v-divider class="my-8 mx-16 pb-8" />
      <v-row>
        <v-col md="3" sm="6" xs="12">
          <v-card>
            <v-card-title class="_darkteal"> Languages </v-card-title>
            <v-card-text class="px-0 pb-0">
              <v-list>
                <v-list-item v-for="item in languages" :key="item.text">
                  <v-list-item-content>
                    <v-list-item-subtitle>{{ item.text }}</v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-icon>
                    <v-chip
                      class="font-weight-bold"
                      small
                      :color="levelColor(item.level)"
                    >
                      {{ item.level }}
                    </v-chip>
                  </v-list-item-icon>
                </v-list-item>
              </v-list>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col md="3" sm="6" xs="12">
          <v-card>
            <v-card-title class="_darkteal"> Databases </v-card-title>
            <v-card-text class="px-0 pb-0">
              <v-list>
                <v-list-item v-for="item in databases" :key="item.text">
                  <v-list-item-content>
                    <v-list-item-subtitle>{{ item.text }}</v-list-item-subtitle>
                  </v-list-item-content>
                  <v-list-item-icon>
                    <v-chip
                      class="font-weight-bold"
                      small
                      :color="levelColor(item.level)"
                    >
                      {{ item.level }}
                    </v-chip>
                  </v-list-item-icon>
                </v-list-item>
              </v-list>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col md="6" sm="12" xs="12">
          <v-card>
            <v-card-title class="_darkteal"> Software </v-card-title>
            <v-card-text class="px-0 pb-0">
              <v-row>
                <v-col cols="6">
                  <v-list>
                    <v-list-item v-for="item in software1" :key="item.text">
                      <v-list-item-content>
                        <v-list-item-subtitle>{{
                          item.text
                        }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                </v-col>
                <v-col cols="6">
                  <v-list>
                    <v-list-item v-for="item in software2" :key="item.text">
                      <v-list-item-content>
                        <v-list-item-subtitle>{{
                          item.text
                        }}</v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      languages: [
        {
          text: 'Python',
          level: 3,
        },
        {
          text: 'Javascript',
          level: 3,
        },
        {
          text: 'PHP',
          level: 2,
        },
        {
          text: 'C++',
          level: 1,
        },
      ],
      databases: [
        {
          text: 'MySQL',
          level: 3,
        },
        {
          text: 'MongoDB',
          level: 3,
        },
        {
          text: 'Neo4j',
          level: 3,
        },
        {
          text: 'Prometheus',
          level: 2,
        },
        {
          text: 'JanusGraph',
          level: 2,
        },
        {
          text: 'Firebase',
          level: 1,
        },
        {
          text: 'Elasticsearch',
          level: 1,
        },
      ],
      software1: [
        { text: 'Django' },
        { text: 'Flask' },
        { text: 'Celery' },
        { text: 'VueJS' },
        { text: 'NuxtJS' },
        { text: 'GraphQL' },
        { text: 'REST' },
        { text: 'Concourse CI/CD' },
        { text: 'Docker' },
      ],
      software2: [
        { text: 'HTML/CSS' },
        { text: 'Linux' },
        { text: 'Kabana' },
        { text: 'RabbitMQ' },
        { text: 'S3' },
        { text: 'Grafana' },
        { text: 'Kibana' },
        { text: 'Logstash' },
      ],
    }
  },
  methods: {
    levelColor(level) {
      if (level === 3) {
        return 'green'
      } else if (level === 2) {
        return 'blue'
      } else if (level === 1) {
        return 'orange'
      }
    },
  },
}
</script>
