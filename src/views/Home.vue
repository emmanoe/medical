<template>
  <v-app id="inspire">

    <v-main>
      <v-container>
        <v-row>
          <v-col
            v-for="n in nb_projects"
            :key="n"
            cols="4"
          >
            <v-card v-if="n==nb_projects" @click="increaseNbProjects()" height="200">
              <v-layout justify-center style="height:100%">

                <v-tooltip bottom>
                  <template v-slot:activator="{ on, attrs }">
                    <v-icon
                      v-bind="attrs"
                      v-on="on"
                      color="black"
                    >mdi-plus</v-icon>
                  </template>
                  <span>Cliquer ici pour créer un nouveau projet !</span>
                </v-tooltip>
                
              </v-layout>
            </v-card>
            <v-card v-else-if="n>0" height="200"></v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        nb_projects: 1,
      }
    },
    methods: {
      increaseNbProjects: function() {
        this.nb_projects += 1
      }
    }
    //
  }
</script>