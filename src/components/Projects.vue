<template>
  <section id="projects" class="project-section">
    <v-container>
      <v-row>
        <v-col class="text-center">
          <h1 style="font-family: Montserrat, sans-serif; color: rgb(211, 210, 210); font-size: 30px">Projects</h1>
          <v-divider :thickness="2" class="mx-auto border-opacity-50" style="width: 555px; color: rgb(211, 210, 210)"></v-divider>
        </v-col>
      </v-row>
      <v-row dense>
        <v-col cols="12" class="d-flex justify-center" v-for="project in projects" :key="project.title">
          <v-card :title="project.title" variant="outlined" color="white" width="900">
            <v-card-text class="d-flex justify-space-between align-center pb-0">
              <div>{{ project.description }}</div>
              <v-btn color="black" class="custom-btn" :href="project.link" target="_blank">Link</v-btn>
            </v-card-text>
          </v-card>
        </v-col>
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
          title: "Sentiment Analysis of Top View Movies' comments from IMDb",
          description: "Utilizing NLP to extract and recommend the most popular movies of the year based on reviews.",
          link: "https://github.com/hjhjhjhhjhjhhh/movie-recommendation-base-on-imdb-review"
        },
        {
          title: "Mind-Controlled Car",
          description: "Using brain signal data to control the turning movements of a remote-controlled car.",
          link: "https://github.com/kunandkarina/Brain-Computer-Interface"
        }
      ]
    };
  }
};
</script>

<style scoped>
.custom-btn {
  padding: 0 !important;
  margin-left: 16px !important;
  min-width: 0 !important;
}

.v-card-text {
  padding-right: 16px !important;
}
</style>
