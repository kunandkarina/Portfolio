<template>
  <v-app>
    <v-navigation-drawer theme="dark" width="260" expand-on-hover rail permanent>
      <v-list-item height="80" prepend-avatar="/avatar.jpg">
        <v-list-item-content>
          <v-list-item-title class="title mb-3">
            Michael Wang
          </v-list-item-title>
          <v-list-item-subtitle class="mt-3">
            software engineer
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

     <v-list density="compact" nav>
        <v-list-item
          v-for="item in items"
          :key="item.value"
          :prepend-icon="item.icon"
          :title="item.title"
          :value="item.value"
          link
          @click="scrollTo(item.title.toLowerCase())"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main> 
      <!-- <router-view/> -->
      <!-- <slot/> -->
      <About/>
      <Projects/>
      <Education/>
      <Skills/>
      <Contact/>

    </v-main> 
  </v-app>
</template>

<script>
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Education from './components/Education.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'


export default {

  components: { About , Projects, Education, Skills,Contact},
  data() {
    return {
      items: [
        { title: 'About', icon: 'mdi-account-box-outline' },
        { title: 'Projects', icon: 'mdi-apps' },
        { title: 'Education', icon: 'mdi-school-outline' },
        { title: 'Skills', icon: 'mdi-code-tags-check' },
        { title: 'Contact', icon: 'mdi-message-reply-text-outline' },
      ]
    }
  },
  methods:{
    scrollTo(id){
      document.getElementById(id).scrollIntoView({behavior: 'smooth'})
      // this.$scrollTo(`#${id}`, 500, { offset: -50 })
    }
  
  }
}
</script>

<style>
html{
  scroll-behavior: smooth;
}

.v-application{
  background: url(./assets/background.jpg)
}

.v-timeline-item__body {
  padding-left: 0 !important;
}

</style>