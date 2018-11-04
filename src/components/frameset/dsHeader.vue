<template>
  <v-tabs v-model="acmenu" color="primary" slider-color="white">
    <v-tab
      v-for="item in items"
      :style="'padding:0 15px'"
      :key="item"
    >
      {{ item }}
    </v-tab>
  </v-tabs>
</template>

<script>
export default {
  name: 'dsHeader',
  data: () => ({
    acmenu: 0,
    items: [
      'Home', 'Blog', 'Study', 'Diary', 'Playground'
    ]
  })
}
</script>

