<v-row no-gutters>
      <v-col
        v-for="n in (projects.length + 1)"
        :key="n"
        cols="12"
        sm="4"
        style="padding:8px; border: 1px groove"
      >
        <v-card style="height:250px;padding:8px">
          <p style="text-align:center" v-if="n==projects.length + 1">
            <v-icon aria-hidden="false" style="height:24px;width:24px;margin-top: 82px;">
              fa-plus
            </v-icon>
          </p>
          <div style="width: 100%; height:100%;" v-else>
            <!-- Title -->
            <h1 style="font-size:18px; width:calc(100% ) !important;float:left; color:#777777">{{ projects[n - 1].name }}</h1>
            
            <!-- Subtitle -->
            <p style="font-size:10px; color:#777777">{{ projects[n - 1].subtitle }}</p>
            <!-- Profils img -->
            <!-- Linear progress bar -->
            <div style="position:absolute;bottom:0px; width:calc(100% - 16px); height: 50px;border: 1px groove;border-radius:8px;padding:0 10px 0 10px;">
              <span style="color:#777777;font-family: 'Roboto', sans-serif;">Progression: </span>
              <span>23.10.20 - 11.12.20 </span>
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