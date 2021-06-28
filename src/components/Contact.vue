<template>
  <section id="contact" class="contact-section">
    <v-container>
      <v-responsive>
        <v-row>
          <v-col>
            <h1 class="text-center">
              Contact Information
            </h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col sm="6" offset-sm="3" class="d-flex justify-space-around">
            <v-btn icon href="https://github.com/Smeks-ops" class="transparent">
              <img class="contact-icon" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg" />
            </v-btn>
            <v-btn icon href="https://www.linkedin.com/in/osemeke-echenim-b17526159/" class="transparent">
              <img class="contact-icon" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" />
            </v-btn>
            <v-btn icon href="https://twitter.com/smeks123?s=08" class="transparent">
              <img class="contact-icon" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg" />
            </v-btn>
            <v-btn icon href="https://www.instagram.com/echenim_ose/" class="transparent">
              <img class="contact-icon" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg" />
            </v-btn>
          </v-col>
        </v-row>
      </v-responsive>
    </v-container>
  </section>
</template>

<style scoped>
.contact-section {
  background-color: #8ec5fc;
  background-image: linear-gradient(62deg, #8ec5fc 0%, #e0c3fc 100%);
}
.contact-icon {
  height: 30px;
}
</style>
