<template>
  <v-app :style="{background: '#F8F8FF'}">
    <v-row no-gutters>
      <v-col
        v-for="n in (projects.length + 1)"
        :key="n"
        cols="12"
        sm="4"
        style="padding:8px"
      >
        <v-card style="height:200px;padding:8px">
          <p style="text-align:center" v-if="n==projects.length + 1">
            <v-icon aria-hidden="false" style="height:24px;width:24px;margin-top: 82px;">
              fa-plus
            </v-icon>
          </p>
          <div style="width: 100%; height:100%;" v-else>
            <!-- Title -->
            <h1 style="width:calc(100% - 24px) !important;float:left;">{{ projects[n - 1].name }}</h1>
            <v-icon aria-hidden="false" style="height:48px;width:24px;float:left;font-size:1em">
                fa-ellipsis-v
              </v-icon>
            <!-- Subtitle -->
            <p>{{ projects[n - 1].subtitle }}</p>
            <!-- Profils img -->
            <!-- Linear progress bar -->
            <div style="position:absolute;bottom:0px; width:calc(100% - 16px); height: 50px;border: 1px solid black;border-radius:8px;padding:0 10px 0 10px;">
              <span>Progression: </span>
              <span>23.10.20 - 20:15 </span>
              <v-progress-linear
                color="teal"
                buffer-value="0"
                value="20"
                stream
              ></v-progress-linear>
            </div>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
    name: 'HelloWorld',
    data: () => ({
      projects: [
        { name: "Project CDP", subtitle: "A project subtitle", teams: [ { name: "me", img: "me/png/path" } ], progress: 10 }
      ]
    }),
    mounted() {
      console.log(this.projects)
    }
}
</script>
