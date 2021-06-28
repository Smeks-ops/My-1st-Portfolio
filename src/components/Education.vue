<template>
  <section id="education-experience">
    <v-container>
      <v-responsive>
        <v-row>
          <v-col>
            <h1>Experience</h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <v-card max-width="450" class="mx-auto">
              <v-toolbar color="blue" dark>
                <v-toolbar-title>Experience</v-toolbar-title>

                <v-spacer></v-spacer>
              </v-toolbar>

              <v-list three-line>
                <template v-for="(item, index) in items">
                  <v-subheader v-if="item.header" :key="item.header" v-text="item.header"></v-subheader>

                  <v-divider v-else-if="item.divider" :key="index" :inset="item.inset"></v-divider>

                  <v-list-item v-else :key="item.title">
                    <v-list-item-avatar>
                      <v-img :src="item.avatar"></v-img>
                    </v-list-item-avatar>

                    <v-list-item-content>
                      <v-list-item-title v-html="item.title"></v-list-item-title>
                      <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>
                    </v-list-item-content>
                  </v-list-item>
                </template>
              </v-list>
            </v-card>
          </v-col>
        </v-row>
      </v-responsive>
    </v-container>
  </section>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        avatar: "",
        title: "UPBASE - April 2021 to present",
        subtitle: `<span class="text--primary">Fullstack Intern</span> &mdash; Design client-side and server-side web apps`,
      },
      { divider: true, inset: true },
      {
        avatar: "",
        title: "Blutenant Miari - Nov 2020 to April 2021",
        subtitle: `<span class="text--primary">Backend Intern</span> &mdash; Participate in the entire application lifecycle, focusing on coding and debugging.`,
      },
    ],
  }),
};
</script>
