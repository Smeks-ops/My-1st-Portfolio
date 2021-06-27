<template>
  <v-app>
    <template>
      <!-- <v-card height="" width="256" class="mx-auto"> -->
      <v-navigation-drawer width="280px" permanent>
        <v-list-item>
          <!-- <v-list-item-avatar>
            <img src="C:\Users\DELL\Documents\Oses's Projects\Portfolio Website\My-1st-Portfolio\src\images\IMG_20210201_145425.jpg">
          </v-list-item-avatar> -->
          <v-list-item-content>
            <v-list-item-title class="text-h6">
              Osemeke Echenim
            </v-list-item-title>
            <v-list-item-subtitle>
              Software Developer
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense nav>
          <v-list-item v-for="item in items" :key="item.title" link>
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <!-- </v-card> -->
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
        { title: "Education", icon: "mdi-school-outline" },
        { title: "Contact", icon: "mdi-message-text-outline" }],

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
.v-application--wrap {
  flex-direction: row;
}</style
.v-main {
  flex: 1 0;
}
>>
