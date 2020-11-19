<template>
  <div style="margin-left:256px;width:calc(100vw - 256px) !important;height:112px;background-color: #F8F8FF">
    <div style="margin-top:22px;">
    <v-app-bar
      color="#FFFFFF"
      height="78px"
      class="mx-auto rounded-xl"
      style="width:98%;position:relative;"
    >
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-autocomplete

      v-model="select"
      :loading="loading"
      :items="items"
      :search-input.sync="search"
      cache-items
      class="mx-auto rounded-xl"
      flat
      hide-no-data
      hide-details
      label="Rechercher ..."
      solo-inverted
    ></v-autocomplete>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-bell-outline</v-icon>
      </v-btn>

      <v-avatar
        style="margin-left:15px"
        color="primary"
        size="56"
      >
      <img
        alt="Avatar"
        src="https://images.unsplash.com/photo-1581093686959-108b3114cc49?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&ixid=eyJhcHBfaWQiOjcyMDE3fQ&q=85&fmt=jpg&crop=entropy&cs=tinysrgb&w=56"
      >
      </v-avatar>
    </v-app-bar>
    </div>
  </div>
</template>