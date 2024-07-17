<template>
  <section id="about">
    <v-container class="about-container">
      <v-row>
        <v-col class="text-center">
            <h1 style="font-family: Montserrat, sans-serif; color: rgb(211, 210, 210); font-size: 30px">About Me.</h1>
            <v-divider :thickness="2" class="mx-auto border-opacity-50" style="width: 555px; color: rgb(211, 210, 210)"></v-divider>
        </v-col>
      </v-row>
      <v-row>
          <v-col sm="6" class="d-flex justify-center align-center">
              <v-img alt="img" :src="require('../assets/Profile.png')" max-width="400" rounded="circle"/>
          </v-col>
          <v-col sm="6" class="d-flex flex-column justify-center">
              <h1 style="font-family: Montserrat, sans-serif; font-size: 32px;">Hi, I'm Michael Wang</h1>
              <div class="text-container">
                <p>
                  I am an undergraduate student at National Yang Ming Chiao Tung University, majoring in computer science. 
                  I am currently focusing on frontend and backend development and have a strong interest in machine learning and data analysis. 
                  I am seeking internship opportunities. If you are interested in me, please feel free to contact me.
                </p>
                <div class="mt-10">
                  <v-btn
                    class="custom-btn"
                    href="/CV.pdf"
                    target="_blank"
                    append-icon="mdi-account-circle"
                    prepend-icon="mdi-open-in-new"
                  >
                    <template v-slot:prepend>
                      <v-icon color="success"></v-icon>
                    </template>
                    My Resume
                    <template v-slot:append>
                      <v-icon color="warning"></v-icon>
                    </template>
                  </v-btn>
                </div>
              </div>
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
.move-down {
  margin-top: 64px;
}
</style>

<style scoped>
.text-container {
  max-width: 550px;
  font-size: 16px;
  font-family: Montserrat, sans-serif;
  font-weight: 400;
}

.about-container {
  color: white;
}

.custom-btn {
  background-color: rgb(60, 65, 72);
  color: white;
}

</style>