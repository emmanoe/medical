<template>
  <v-card>
      <v-navigation-drawer permanent floating
        color="#F8F8FF"
        app
      >
      <div 
        style="border-radius:10px;width: calc(100% - 20px);height: calc(-40px + 100vh); margin: 20px 0px 0px 10px; background: #FFFFFF;overflow:hidden">
        <v-img
            src="@/assets/applogo.png"
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