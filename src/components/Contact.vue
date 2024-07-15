<template>
  <section id="contact" class="contact-section ">
    <v-container>
      <v-row>
        <v-col class="d-flex align-center">
          <h1 class="custom-heading" >© 2024 Copyright: Michael Wang</h1>
        </v-col>
        <v-col sm="6" offset-sm="3" class="d-flex justify-start">
          <a href="https://github.com/kunandkarina" target="_blank">
            <img class="contact-icon mx-5" src="https://cdn.jsdelivr.net/npm/simple-icons@13.1.0/icons/github.svg">
          </a>
          <a href="https://www.linkedin.com/in/michael-wang-4741042b7/" target="_blank">
            <img class="contact-icon mx-5" src="https://cdn.jsdelivr.net/npm/simple-icons@13.1.0/icons/linkedin.svg">
          </a>
          <a href="mailto:michael60457@gmail.com" target="_blank">
            <img class="contact-icon mx-5" src="https://cdn.jsdelivr.net/npm/simple-icons@13.1.0/icons/gmail.svg">
          </a>
          <a href="https://www.instagram.com/wang_1.2.2.3/" target="_blank">
            <img class="contact-icon mx-5" src="https://cdn.jsdelivr.net/npm/simple-icons@13.1.0/icons/instagram.svg">
          </a>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {

}
</script>

<style>
.contact-section{
    background-color : #888888
}

.contact-icon{
    height : 25px;
}

.custom-heading {
  color: rgb(255, 255, 255);
  font-size: 16px;
  font-weight: 500;
  margin: 0;
  font-family: Montserrat, sans-serif;
}
</style>