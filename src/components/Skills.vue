<template>
  <section id="skills">
    <v-container>
        <v-row>
            <v-col class="text-center">
              <h1 style="font-family: Montserrat, sans-serif; color: rgb(211, 210, 210); font-size: 30px"> Skill </h1>
              <v-divider :thickness="2" class="mx-auto border-opacity-50" style="width: 555px; color: rgb(211, 210, 210)"></v-divider>
            </v-col>
        </v-row>
        <v-row justify="center">
        <v-col v-for="(card, index) in cards" :key="index" cols="6" class="d-flex">
          <v-card class="mx-auto d-flex flex-column align-center custom-card" height="300" width="400" color="#343a40">
            <v-card-title class="text-center">{{ card.title }}</v-card-title>
            <v-icon :icon="card.icon" size="large" class="mt-n2"></v-icon>
            <v-card-text v-if="card.title === 'Languages'" class="text-center d-flex justify-center">
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg" class="icon mr-4"/>
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original-wordmark.svg" class="icon mx-4"/>
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" class="icon ml-4"/>
            </v-card-text>
            <v-card-text v-if="card.title === 'Front-end'" class="text-center d-flex justify-center">
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original-wordmark.svg" class="icon mr-4"/>
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original-wordmark.svg" class="icon mx-4"/>
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original-wordmark.svg" class="icon ml-4"/>
            </v-card-text>
            <v-card-text v-if="card.title === 'Database'" class="text-center d-flex justify-center">
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original-wordmark.svg" class="icon"/>
            </v-card-text>
            <v-card-text v-if="card.title === 'Others'" class="text-center d-flex justify-center">
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" class="icon mr-4"/>
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/blender/blender-original.svg" class="icon mx-4"/>
              <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original-wordmark.svg" class="icon ml-4"/>
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
      cards: [
        { title: 'Languages', icon: 'mdi-code-tags' },
        { title: 'Front-end', icon: 'mdi-monitor-dashboard' },
        { title: 'Database', icon: 'mdi-database-cog-outline' },
        { title: 'Others', icon: 'mdi-cog-outline' },
      ],
    }
  },
}
</script>

<style scoped>

.custom-card {
  border: 2px solid rgba(255, 255, 255, 0.1);
  transition: all 0.3s ease;
  overflow: hidden;
  position: relative;
}

.custom-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
  transform: translateX(-100%);
  transition: 0.6s;
}

.custom-card:hover {
  transform: scale(1.05);
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
}

.custom-card:hover::before {
  transform: translateX(100%);
}

.icon{
  width: 50px;
  height: 50px;
  transition: transform 0.3s ease;
}

.custom-card:hover .icon{
  transform: scale(1.1);
}

</style>