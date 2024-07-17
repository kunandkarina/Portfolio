<template>
  <section id="education">
    <v-container>
      <v-row>
        <v-col class="text-center">
          <h1 style="font-family: Montserrat, sans-serif; color: rgb(211, 210, 210); font-size: 30px">Education</h1>
          <v-divider :thickness="2" class="mx-auto border-opacity-50" style="width: 555px; color: rgb(211, 210, 210)"></v-divider>
        </v-col>
      </v-row>
      <v-row justify="center"> 
        <v-col cols="12" md="8">
          <v-timeline align="start" line-color="white">
            <v-timeline-item
              v-for="(item, i) in educationItems"
              :key="i"
              :dot-color="item.color"
              size="small"
            >
              <template v-slot:opposite>
                <div
                  :class="`pt-1 headline font-weight-bold text-${item.color}`"
                  v-text="item.year"
                ></div>
              </template>
              <div class="content-wrapper">
                <div :class="`institution-text text-${item.color}`">
                  {{ item.institution }}
                </div>
                <div class="description-text">
                  {{ item.description }}
                </div>
                <div class="date-text">
                  {{ item.date }}
                </div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data: () => ({
    educationItems: [
      {
        color: 'cyan',
        year: '2021',
        institution: 'NYCU, Hsinchu, Taiwan',
        description: 'bachelor in computer science',
        date: 'sep, 2021-present'
      },
    ],
  }),
}
</script>

<style scoped>
.content-wrapper {
  max-width: 250px;
  margin: 0 auto;
}

.institution-text {
  font-family: Montserrat, sans-serif;
  font-size: 20px;
  font-weight: 400;
}

.description-text {
  color: rgb(211, 210, 210);
  font-family: Montserrat, sans-serif;
  font-size: 16px;
  font-weight: 400;
}

.date-text {
  color: rgb(211, 210, 210);
  font-family: Montserrat, sans-serif;
  font-size: 14px;
  font-weight: 300;
}

</style>