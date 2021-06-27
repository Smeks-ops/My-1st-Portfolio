<template>
  <section id="projects" class="project-section">
    <v-container>
      <v-row>
        <v-col>
          <h1>Projects</h1>
        </v-col>
      </v-row>
      <v-row class="justify-space-around mb-8 mt-4">
        <v-card v-for="project in projects" :key="project.name" class="" max-width="300">
          <v-img class="align-end" height="200px" :src="project.image" />
          <v-card-title>{{ project.name }}</v-card-title>

          <v-card-text class="text--primary">
            {{ truncate(project.description) }}
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text :href="project.github">
              Github repo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "WYSIWYG",
          github: "https://github.com/Smeks-ops/WYSIWYG",
          description:
            "A webpage that fetches data from an api endpoint (https://api.binance.com/api/v3/ticker/24hr) every 30 seconds, stores it in a vuex store and displays the historical data retrieved and stored for each symbol through its own page route",
          image: "https://github.com/Smeks-ops/WYSIWYG/blob/main/wysiwyg%202.png?raw=true",
        },
        {
          name: "GIGO",
          github: "https://github.com/Smeks-ops/TEAM-GIGO-CODING-CHALLENGE",
          description:
            "An api service that fetches data from an api endpoint every 30 seconds and stores it in a database table and also displays the historical data retrieved and stored for each symbol through its own unique endpoint.",
          image: "https://github.com/Smeks-ops/TEAM-GIGO-CODING-CHALLENGE/blob/main/gigo-binance.png?raw=true",
        },
        {
          name: "Monster Slayer",
          github: "https://github.com/Smeks-ops/Simple-Monster-Slayer-Game",
          description: "A web game app made with Vuejs and Javascript",
          image: "https://github.com/Smeks-ops/Simple-Monster-Slayer-Game/blob/main/Monster%20Slayer.png?raw=true",
        },
      ],
    };
  },
  methods: {
    truncate(str) {
      if (str.length > 80) {
        return str.slice(0, 79) + "...";
      }
      return str;
    },
  },
};
</script>
<style scoped>
.project-section {
  background-color: #4158d0;
  background-image: linear-gradient(43deg, #4158d0 0%, #c850c0 46%, #ffcc70 100%);
}
</style>
