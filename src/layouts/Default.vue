<template>
  <v-app>
    <template>
      <v-navigation-drawer width="240px" permanent fixed>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title">
              Osemeke Echenim
            </v-list-item-title>
            <v-list-item-subtitle>
              Jnr. Web Developer
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense nav>
          <v-list-item v-for="item in items" :key="item.title" link :to="`#${item.title.toLowerCase().replace(' & ', '-')}`">
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </template>
    <v-main>
      <slot />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "About", icon: "mdi-account-box-outline" },
        { title: "Projects", icon: "mdi-apps" },
        { title: "Experience", icon: "mdi-school-outline" },
        { title: "Contact", icon: "mdi-message-text-outline" },
      ],
    };
  },
};
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
html {
  scroll-behavior: smooth;
}
.v-application--wrap {
  flex-direction: row;
}
.v-main {
  flex: 1 0;
  margin-left: 280px;
}
</style>
