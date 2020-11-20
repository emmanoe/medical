<template>
  <v-card>
      <v-navigation-drawer permanent floating
        color="#F8F8FF"
        app
      >
      <div 
        style=" height: 99%; border-radius:20px; background: #FFFFFF;overflow:hidden">
        <v-img
            src="@/assets/applogo.png"
            height="10%"
        ></v-img>

          <v-divider></v-divider>

          <v-list dense>
            <v-list-item class="title"
              v-for="item in items"
              :key="item.title"
              link
            >
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </div>
      </v-navigation-drawer>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Menu', icon: 'mdi-menu' },
          { title: 'Projets', icon: 'mdi-briefcase' },
          { title: 'Gestion des tests', icon: 'mdi-test-tube' },
        ],
        mini: false,
      }
    },
  }
</script>